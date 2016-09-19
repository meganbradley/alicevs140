---
title: "How to: Convert an OpenMP Loop that Uses Cancellation to Use the Concurrency Runtime"
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
ms.assetid: 4b0b3c33-bfa9-4e96-ae08-aef245a39cbb
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Convert an OpenMP Loop that Uses Cancellation to Use the Concurrency Runtime
Some parallel loops do not require that all iterations be executed. For example, an algorithm that searches for a value can terminate after the value is found. OpenMP does not provide a mechanism to break out of a parallel loop. However, you can use a Boolean value, or flag, to enable an iteration of the loop to indicate that the solution has been found. The Concurrency Runtime provides functionality that enables one task to cancel other tasks that have not yet started.  
  
 This example demonstrates how to convert an OpenMP [parallel](../vs140/parallel.md)[for](../vs140/for--OpenMP-.md) loop that does not require for all iterations to run to use the Concurrency Runtime cancellation mechanism.  
  
## Example  
 This example uses both OpenMP and the Concurrency Runtime to implement a parallel version of the [std::any_of](../vs140/any_of.md) algorithm. The OpenMP version of this example uses a flag to coordinate among all parallel loop iterations that the condition has been met. The version that uses the Concurrency Runtime uses the [concurrency::structured_task_group::cancel](../vs140/structured_task_group--cancel-Method.md) method to stop the overall operation when the condition is met.  
  
 [!CODE [concrt-openmp#2](../CodeSnippet/VS_Snippets_ConcRT/concrt-openmp#2)]  
  
 This example produces the following output.  
  
 **Using OpenMP...**  
**9114046 is in the array.**  
**Using the Concurrency Runtime...**  
**9114046 is in the array.** In the version of that uses OpenMP, all iterations of the loop execute, even when the flag is set. Furthermore, if a task were to have any child tasks, the flag would also have to be available to those child tasks to communicate cancellation. In the Concurrency Runtime, when a task group is cancelled, the runtime cancels the entire tree of work, including child tasks. The [concurrency::parallel_for_each](../vs140/parallel_for_each-Function.md) algorithm uses tasks to perform work. Therefore, when one iteration of the loop cancels the root task, the entire tree of computation is also cancelled. When a tree of work is cancelled, the runtime does not start new tasks. However, the runtime allows tasks that have already started to finish. Therefore, in the case of the `parallel_for_each` algorithm, active loop iterations can clean up their resources.  
  
 In both versions of this example, if the array contains more than one copy of the value to search for, multiple loop iterations can each simultaneously set the result and cancel the overall operation. You can use a synchronization primitive, such as a critical section, if your problem requires that only one task performs work when a condition is met.  
  
 You can also use exception handling to cancel tasks that use the PPL. For more information about cancellation, see [Cancellation in the PPL](../vs140/Cancellation-in-the-PPL.md).  
  
 For more information about `parallel_for_each` and other parallel algorithms, see [Parallel Algorithms](../vs140/Parallel-Algorithms.md).  
  
## Compiling the Code  
 Copy the example code and paste it in a Visual Studio project, or paste it in a file that is named `concrt-omp-parallel-any-of.cpp` and then run the following command in a Visual Studio Command Prompt window.  
  
 **cl.exe /EHsc /openmp concrt-omp-parallel-any-of.cpp**  
  
## See Also  
 [Migrating from OpenMP to the Concurrency Runtime](../vs140/Migrating-from-OpenMP-to-the-Concurrency-Runtime.md)   
 [Cancellation in the PPL](../vs140/Cancellation-in-the-PPL.md)   
 [Parallel Algorithms](../vs140/Parallel-Algorithms.md)