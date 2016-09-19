---
title: "How to: Use parallel_invoke to Execute Parallel Operations"
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
ms.assetid: a6aea69b-d647-4b7e-bf3b-e6a6a9880072
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Use parallel_invoke to Execute Parallel Operations
This example shows how to use the [concurrency::parallel_invoke](../vs140/parallel_invoke-Function.md) algorithm to improve the performance of a program that performs multiple operations on a shared data source. Because no operations modify the source, they can be executed in parallel in a straightforward manner.  
  
## Example  
 Consider the following code example that creates a variable of type `MyDataType`, calls a function to initialize that variable, and then performs multiple lengthy operations on that data.  
  
 [!CODE [concrt-parallel-word-mining#1](../CodeSnippet/VS_Snippets_ConcRT/concrt-parallel-word-mining#1)]  
  
 If the `lengthy_operation1`, `lengthy_operation2`, and `lengthy_operation3` functions do not modify the `MyDataType` variable, these functions can be executed in parallel without additional modifications.  
  
## Example  
 The following example modifies the previous example to run in parallel. The `parallel_invoke` algorithm executes each task in parallel and returns after all tasks are finished.  
  
 [!CODE [concrt-parallel-word-mining#2](../CodeSnippet/VS_Snippets_ConcRT/concrt-parallel-word-mining#2)]  
  
## Example  
 The following example downloads *The Iliad* by Homer from gutenberg.org and performs multiple operations on that file. The example first performs these operations serially and then performs the same operations in parallel.  
  
 [!CODE [concrt-parallel-word-mining#3](../CodeSnippet/VS_Snippets_ConcRT/concrt-parallel-word-mining#3)]  
  
 This example produces the following sample output.  
  
 **Downloading 'The Iliad'...**  
**Running serial version... took 953 ms.**  
**Running parallel version... took 656 ms.**  
**The most common words that have five or more letters are:**  
 **their (953)**  
 **shall (444)**  
 **which (431)**  
 **great (398)**  
 **Hector (349)**  
 **Achilles (309)**  
 **through (301)**  
 **these (268)**  
 **chief (259)**  
**The longest sequence of words that have the same first letter is:**  
 **through the tempest to the tented**  
**The following palindromes appear in the text:**  
 **spots stops**  
 **speed deeps**  
 **keels sleek** This example uses the `parallel_invoke` algorithm to call multiple functions that act on the same data source. You can use the `parallel_invoke` algorithm to call any set of functions in parallel, not only those that act on the same data.  
  
 Because the `parallel_invoke` algorithm calls each work function in parallel, its performance is bounded by the function that takes the longest time to finish (that is, if the runtime processes each function on a separate processor). If this example performs more tasks in parallel than the number of available processors, multiple tasks can run on each processor. In this case, performance is bounded by the group of tasks that takes the longest time to finish.  
  
 Because this example performs three tasks in parallel, you should not expect performance to scale on computers that have more than three processors. To improve performance more, you can break the longest-running tasks into smaller tasks and run those tasks in parallel.  
  
 You can use the `parallel_invoke` algorithm instead of the [concurrency::task_group](../vs140/task_group-Class.md) and [concurrency::structured_task_group](../vs140/structured_task_group-Class.md) classes if you do not require support for cancellation. For an example that compares the usage of the `parallel_invoke` algorithm versus task groups, see [Walkthrough: Using Task Groups to Improve Performance](../vs140/How-to--Use-parallel_invoke-to-Write-a-Parallel-Sort-Routine.md).  
  
## Compiling the Code  
 To compile the code, copy it and then paste it in a Visual Studio project, or paste it in a file that is named `parallel-word-mining.cpp` and then run the following command in a Visual Studio Command Prompt window.  
  
 **cl.exe /EHsc /MD /DUNICODE /D_AFXDLL parallel-word-mining.cpp**  
  
## See Also  
 [Parallel Algorithms](../vs140/Parallel-Algorithms.md)   
 [parallel_invoke Function](../vs140/parallel_invoke-Function.md)