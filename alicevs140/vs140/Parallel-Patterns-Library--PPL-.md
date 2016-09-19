---
title: "Parallel Patterns Library (PPL)"
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
ms.assetid: 40fd86b2-69fa-45e5-93d8-98a75636c242
caps.latest.revision: 23
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Parallel Patterns Library (PPL)
The Parallel Patterns Library (PPL) provides an imperative programming model that promotes scalability and ease-of-use for developing concurrent applications. The PPL builds on the scheduling and resource management components of the Concurrency Runtime. It raises the level of abstraction between your application code and the underlying threading mechanism by providing generic, type-safe algorithms and containers that act on data in parallel. The PPL also lets you develop applications that scale by providing alternatives to shared state.  
  
 The PPL provides the following features:  
  
-   *Task Parallelism*: a mechanism that works on top of the Windows ThreadPool to execute several work items (tasks) in parallel  
  
-   *Parallel algorithms*: generic algorithms that works on top of the Concurrency Runtime to act on collections of data in parallel  
  
-   *Parallel containers and objects*: generic container types that provide safe concurrent access to their elements  
  
## Example  
 The PPL provides a programming model that resembles the Standard Template Library (STL). The following example demonstrates many features of the PPL. It computes several Fibonacci numbers serially and in parallel. Both computations act on a [std::array](../vs140/array-Class--STL-.md) object. The example also prints to the console the time that is required to perform both computations.  
  
 The serial version uses the STL [std::for_each](../vs140/for_each.md) algorithm to traverse the array and stores the results in a [std::vector](../vs140/vector-Class.md) object. The parallel version performs the same task, but uses the PPL [concurrency::parallel_for_each](../vs140/parallel_for_each-Function.md) algorithm and stores the results in a [concurrency::concurrent_vector](../vs140/concurrent_vector-Class.md) object. The `concurrent_vector` class enables each loop iteration to concurrently add elements without the requirement to synchronize write access to the container.  
  
 Because `parallel_for_each` acts concurrently, the parallel version of this example must sort the `concurrent_vector` object to produce the same results as the serial version.  
  
 Note that the example uses a naïve method to compute the Fibonacci numbers; however, this method illustrates how the Concurrency Runtime can improve the performance of long computations.  
  
 [!CODE [concrt-parallel-fibonacci#1](../CodeSnippet/VS_Snippets_ConcRT/concrt-parallel-fibonacci#1)]  
  
 The following sample output is for a computer that has four processors.  
  
 **serial time: 9250 ms**  
**parallel time: 5726 ms**  
**fib(24): 46368**  
**fib(26): 121393**  
**fib(41): 165580141**  
**fib(42): 267914296** Each iteration of the loop requires a different amount of time to finish. The performance of `parallel_for_each` is bounded by the operation that finishes last. Therefore, you should not expect linear performance improvements between the serial and parallel versions of this example.  
  
## Related Topics  
  
|Title|Description|  
|-----------|-----------------|  
|[Task Parallelism](../vs140/Task-Parallelism--Concurrency-Runtime-.md)|Describes the role of tasks and task groups in the PPL.|  
|[Parallel Algorithms](../vs140/Parallel-Algorithms.md)|Describes how to use parallel algorithms such as `parallel_for` and `parallel_for_each`.|  
|[Parallel Containers and Objects](../vs140/Parallel-Containers-and-Objects.md)|Describes the various parallel containers and objects that are provided by the PPL.|  
|[Cancelation](../vs140/Cancellation-in-the-PPL.md)|Explains how to cancel the work that is being performed by a parallel algorithm.|  
|[Concurrency Runtime](../vs140/Concurrency-Runtime.md)|Describes the Concurrency Runtime, which simplifies parallel programming, and contains links to related topics.|