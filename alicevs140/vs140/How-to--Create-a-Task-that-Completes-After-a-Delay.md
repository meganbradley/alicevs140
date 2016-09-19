---
title: "How to: Create a Task that Completes After a Delay"
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
ms.assetid: 3fc0a194-3fdb-4eba-8b8a-b890981a985d
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Create a Task that Completes After a Delay
This example shows how to use the [concurrency::task](../vs140/task-Class--Concurrency-Runtime-.md), [concurrency::cancellation_token_source](../vs140/cancellation_token_source-Class.md), [concurrency::cancellation_token](../vs140/cancellation_token-Class.md), [concurrency::task_completion_event](../vs140/task_completion_event-Class.md), [concurrency::timer](../vs140/timer-Class.md), and [concurrency::call](../vs140/call-Class.md) classes to create a task that completes after a delay. You can use this method to build loops that occasionally poll for data, introduce timeouts, delay handling of user input for a predetermined time, and so on.  
  
## Example  
 The following example shows the `complete_after` and `cancel_after_timeout` functions. The `complete_after` function creates a `task` object that completes after the specified delay. It uses a `timer` object and a `call` object to set a `task_completion_event` object after the specified delay. By using the `task_completion_event` class, you can define a task that completes after a thread or another task signals that a value is available. When the event is set, listener tasks complete and their continuations are scheduled to run.  
  
> [!TIP]
>  For more information about the `timer` and `call` classes, which are part of the Asynchronous Agents Library, see [Asynchronous Message Blocks](../vs140/Asynchronous-Message-Blocks.md).  
  
 The `cancel_after_timeout` function builds on the `complete_after` function to cancel a task if that task does not complete before a given timeout. The `cancel_after_timeout` function creates two tasks. The first task indicates success and completes after the provided task completes; the second task indicates failure and completes after the specified timeout. The `cancel_after_timeout` function creates a continuation task that runs when the success or failure task completes. If the failure task completes first, the continuation cancels the token source to cancel the overall task.  
  
 [!CODE [concrt-task-delay#1](../CodeSnippet/VS_Snippets_ConcRT/concrt-task-delay#1)]  
  
## Example  
 The following example computes the count of prime numbers in the range [0, 100000] multiple times. The operation fails if it does not complete in a given time limit. The `count_primes` function demonstrates how to use the `cancel_after_timeout` function. It counts the number of primes in the given range and fails if the task does not complete in the provided time. The `wmain` function calls the `count_primes` function multiple times. Each time, it halves the time limit. The program finishes after the operation does not complete in the current time limit.  
  
 [!CODE [concrt-task-delay#2](../CodeSnippet/VS_Snippets_ConcRT/concrt-task-delay#2)]  
  
 When you use this technique to cancel tasks after a delay, any unstarted tasks will not start after the overall task is canceled. However, it is important for any long-running tasks to respond to cancellation in a timely manner. In this example, the `count_primes` method calls the [concurrency::is_task_cancellation_requested](../vs140/is_task_cancellation_requested-Function.md) and `cancel_current_task` functions to respond to cancellation. (Alternatively, you can call the [concurrency::interruption_point](../vs140/interruption_point-Function.md) function). For more information about task cancellation, see [Cancellation in the PPL](../vs140/Cancellation-in-the-PPL.md).  
  
## Example  
 Here is the complete code for this example:  
  
 [!CODE [concrt-task-delay#3](../CodeSnippet/VS_Snippets_ConcRT/concrt-task-delay#3)]  
  
## Compiling the Code  
 To compile the code, copy it and then paste it in a Visual Studio project, or paste it in a file that is named `task-delay.cpp` and then run the following command in a Visual Studio Command Prompt window.  
  
 **cl.exe /EHsc task-delay.cpp**  
  
## See Also  
 [Task Parallelism (Concurrency Runtime)](../vs140/Task-Parallelism--Concurrency-Runtime-.md)   
 [task Class](../vs140/task-Class--Concurrency-Runtime-.md)   
 [cancellation_token_source Class](../vs140/cancellation_token_source-Class.md)   
 [cancellation_token Class](../vs140/cancellation_token-Class.md)   
 [task_completion_event Class](../vs140/task_completion_event-Class.md)   
 [is_task_cancellation_requested Function](../vs140/is_task_cancellation_requested-Function.md)   
 [cancel_current_task Function](../vs140/cancel_current_task-Function.md)   
 [interruption_point Function](../vs140/interruption_point-Function.md)   
 [timer Class](../vs140/timer-Class.md)   
 [call Class](../vs140/call-Class.md)   
 [Asynchronous Message Blocks](../vs140/Asynchronous-Message-Blocks.md)   
 [Cancellation in the PPL](../vs140/Cancellation-in-the-PPL.md)