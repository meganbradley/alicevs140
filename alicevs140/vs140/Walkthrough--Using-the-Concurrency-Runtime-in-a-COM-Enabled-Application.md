---
title: "Walkthrough: Using the Concurrency Runtime in a COM-Enabled Application"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: a7c798b8-0fc8-4bee-972f-22ef158f7f48
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Walkthrough: Using the Concurrency Runtime in a COM-Enabled Application
This document demonstrates how to use the Concurrency Runtime in an application that uses the Component Object Model (COM).  
  
## Prerequisites  
 Read the following documents before you start this walkthrough:  
  
-   [Task Parallelism (Concurrency Runtime)](../vs140/Task-Parallelism--Concurrency-Runtime-.md)  
  
-   [Parallel Algorithms](../vs140/Parallel-Algorithms.md)  
  
-   [Asynchronous Agents](../vs140/Asynchronous-Agents.md)  
  
-   [Exception Handling in the Concurrency Runtime](../vs140/Exception-Handling-in-the-Concurrency-Runtime.md)  
  
 For more information about COM, see [Component Object Model (COM)](http://msdn.microsoft.com/library/windows/desktop/ms680573).  
  
## Managing the Lifetime of the COM Library  
 Although the use of COM with the Concurrency Runtime follows the same principles as any other concurrency mechanism, the following guidelines can help you use these libraries together effectively.  
  
-   A thread must call [CoInitializeEx](http://msdn.microsoft.com/library/windows/desktop/ms695279) before it uses the COM library.  
  
-   A thread can call `CoInitializeEx` multiple times as long as it provides the same arguments to every call.  
  
-   For each call to `CoInitializeEx`, a thread must also call [CoUninitialize](http://msdn.microsoft.com/library/windows/desktop/ms688715). In other words, calls to `CoInitializeEx` and `CoUninitialize` must be balanced.  
  
-   To switch from one thread apartment to another, a thread must completely free the COM library before it calls `CoInitializeEx` with the new threading specification.  
  
 Other COM principles apply when you use COM with the Concurrency Runtime. For example, an application that creates an object in a single-threaded apartment (STA) and marshals that object to another apartment must also provide a message loop to process incoming messages. Also remember that marshaling objects between apartments can decrease performance.  
  
### Using COM with the Parallel Patterns Library  
 When you use COM with a component in the Parallel Patterns Library (PPL), for example, a task group or parallel algorithm, call `CoInitializeEx` before you use the COM library during each task or iteration, and call `CoUninitialize` before each task or iteration finishes. The following example shows how to manage the lifetime of the COM library with a [concurrency::structured_task_group](../vs140/structured_task_group-Class.md) object.  
  
 [!CODE [concrt-parallel-scripts#1](../CodeSnippet/VS_Snippets_ConcRT/concrt-parallel-scripts#1)]  
  
 You must make sure that the COM library is correctly freed when a task or parallel algorithm is canceled or when the task body throws an exception. To guarantee that the task calls `CoUninitialize` before it exits, use a `try-finally` block or the *Resource Acquisition Is Initialization* (RAII) pattern. The following example uses a `try-finally` block to free the COM library when the task completes or is canceled, or when an exception is thrown.  
  
 [!CODE [concrt-parallel-scripts#2](../CodeSnippet/VS_Snippets_ConcRT/concrt-parallel-scripts#2)]  
  
 The following example uses the RAII pattern to define the `CCoInitializer` class, which manages the lifetime of the COM library in a given scope.  
  
 [!CODE [concrt-parallel-scripts#3](../CodeSnippet/VS_Snippets_ConcRT/concrt-parallel-scripts#3)]  
  
 You can use the `CCoInitializer` class to automatically free the COM library when the task exits, as follows.  
  
 [!CODE [concrt-parallel-scripts#4](../CodeSnippet/VS_Snippets_ConcRT/concrt-parallel-scripts#4)]  
  
 For more information about cancellation in the Concurrency Runtime, see [Cancellation in the PPL](../vs140/Cancellation-in-the-PPL.md).  
  
### Using COM with Asynchronous Agents  
 When you use COM with asynchronous agents, call `CoInitializeEx` before you use the COM library in the [concurrency::agent::run](../vs140/agent--run-Method.md) method for your agent. Then call `CoUninitialize` before the `run` method returns. Do not use COM management routines in the constructor or destructor of your agent, and do not override the [concurrency::agent::start](../vs140/agent--start-Method.md) or [concurrency::agent::done](../vs140/agent--done-Method.md) methods because these methods are called from a different thread than the `run` method.  
  
 The following example shows a basic agent class, named `CCoAgent`, which manages the COM library in the `run` method.  
  
 [!CODE [concrt-parallel-scripts#5](../CodeSnippet/VS_Snippets_ConcRT/concrt-parallel-scripts#5)]  
  
 A complete example is provided later in this walkthrough.  
  
### Using COM with Lightweight Tasks  
 The document [Task Scheduler (Concurrency Runtime)](../vs140/Task-Scheduler--Concurrency-Runtime-.md) describes the role of lightweight tasks in the Concurrency Runtime. You can use COM with a lightweight task just as you would with any thread routine that you pass to the `CreateThread` function in the Windows API. This is shown in the following example.  
  
 [!CODE [concrt-parallel-scripts#6](../CodeSnippet/VS_Snippets_ConcRT/concrt-parallel-scripts#6)]  
  
## An Example of a COM-Enabled Application  
 This section shows a complete COM-enabled application that uses the `IScriptControl` interface to execute a script that computes the n<sup>th</sup> Fibonacci number. This example first calls the script from the main thread, and then uses the PPL and agents to call the script concurrently.  
  
 Consider the following helper function, `RunScriptProcedure`, which calls a procedure in an `IScriptControl` object.  
  
 [!CODE [concrt-parallel-scripts#7](../CodeSnippet/VS_Snippets_ConcRT/concrt-parallel-scripts#7)]  
  
 The `wmain` function creates an `IScriptControl` object, adds script code to it that computes the n<sup>th</sup> Fibonacci number, and then calls the `RunScriptProcedure` function to run that script.  
  
 [!CODE [concrt-parallel-scripts#8](../CodeSnippet/VS_Snippets_ConcRT/concrt-parallel-scripts#8)]  
  
### Calling the Script from the PPL  
 The following function, `ParallelFibonacci`, uses the [concurrency::parallel_for](../vs140/parallel_for-Function.md) algorithm to call the script in parallel. This function uses the `CCoInitializer` class to manage the lifetime of the COM library during every iteration of the task.  
  
 [!CODE [concrt-parallel-scripts#9](../CodeSnippet/VS_Snippets_ConcRT/concrt-parallel-scripts#9)]  
  
 To use the `ParallelFibonacci` function with the example, add the following code before the `wmain` function returns.  
  
 [!CODE [concrt-parallel-scripts#10](../CodeSnippet/VS_Snippets_ConcRT/concrt-parallel-scripts#10)]  
  
### Calling the Script from an Agent  
 The following example shows the `FibonacciScriptAgent` class, which calls a script procedure to compute the n<sup>th</sup> Fibonacci number. The `FibonacciScriptAgent` class uses message passing to receive, from the main program, input values to the script function. The `run` method manages the lifetime of the COM library throughout the task.  
  
 [!CODE [concrt-parallel-scripts#11](../CodeSnippet/VS_Snippets_ConcRT/concrt-parallel-scripts#11)]  
  
 The following function, `AgentFibonacci`, creates several `FibonacciScriptAgent` objects and uses message passing to send several input values to those objects.  
  
 [!CODE [concrt-parallel-scripts#12](../CodeSnippet/VS_Snippets_ConcRT/concrt-parallel-scripts#12)]  
  
 To use the `AgentFibonacci` function with the example, add the following code before the `wmain` function returns.  
  
 [!CODE [concrt-parallel-scripts#13](../CodeSnippet/VS_Snippets_ConcRT/concrt-parallel-scripts#13)]  
  
### The Complete Example  
 The following code shows the complete example, which uses parallel algorithms and asynchronous agents to call a script procedure that computes Fibonacci numbers.  
  
 [!CODE [concrt-parallel-scripts#14](../CodeSnippet/VS_Snippets_ConcRT/concrt-parallel-scripts#14)]  
  
 The example produces the following sample output.  
  
 **Main Thread:**  
**fib(15) = 610**  
**Parallel Fibonacci:**  
**fib(15) = 610**  
**fib(10) = 55**  
**fib(16) = 987**  
**fib(18) = 2584**  
**fib(11) = 89**  
**fib(17) = 1597**  
**fib(19) = 4181**  
**fib(12) = 144**  
**fib(13) = 233**  
**fib(14) = 377**  
**Agent Fibonacci:**  
**fib(30) = 832040**  
**fib(22) = 17711**  
**fib(10) = 55**  
**fib(12) = 144**   
## Compiling the Code  
 Copy the example code and paste it in a Visual Studio project, or paste it in a file that is named `parallel-scripts.cpp` and then run the following command in a Visual Studio Command Prompt window.  
  
 **cl.exe /EHsc parallel-scripts.cpp /link ole32.lib**  
  
## See Also  
 [Advanced How-to and Walkthrough Topics](../vs140/Concurrency-Runtime-Walkthroughs.md)   
 [Task Parallelism (Concurrency Runtime)](../vs140/Task-Parallelism--Concurrency-Runtime-.md)   
 [Parallel Algorithms](../vs140/Parallel-Algorithms.md)   
 [Asynchronous Agents](../vs140/Asynchronous-Agents.md)   
 [Exception Handling in the Concurrency Runtime](../vs140/Exception-Handling-in-the-Concurrency-Runtime.md)   
 [Cancellation in the PPL](../vs140/Cancellation-in-the-PPL.md)   
 [Task Scheduler (Concurrency Runtime)](../vs140/Task-Scheduler--Concurrency-Runtime-.md)