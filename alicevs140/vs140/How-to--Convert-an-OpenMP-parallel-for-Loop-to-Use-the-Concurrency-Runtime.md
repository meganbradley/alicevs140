---
title: "How to: Convert an OpenMP parallel for Loop to Use the Concurrency Runtime"
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
ms.assetid: d8a7b656-f86c-456e-9c5d-a7d52f94646e
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Convert an OpenMP parallel for Loop to Use the Concurrency Runtime
This example demonstrates how to convert a basic loop that uses the OpenMP [parallel](../vs140/parallel.md) and [for](../vs140/for--OpenMP-.md) directives to use the Concurrency Runtime [concurrency::parallel_for](../vs140/parallel_for-Function.md) algorithm.  
  
## Example  
 This example uses both OpenMP and the Concurrency Runtime to compute the count of prime numbers in an array of random values.  
  
 [!CODE [concrt-openmp#1](../CodeSnippet/VS_Snippets_ConcRT/concrt-openmp#1)]  
  
 This example produces the following output.  
  
 **Using OpenMP...**  
**found 107254 prime numbers.**  
**Using the Concurrency Runtime...**  
**found 107254 prime numbers.** The `parallel_for` algorithm and OpenMP 3.0 allow for the index type to be a signed integral type or an unsigned integral type. The `parallel_for` algorithm also makes sure that the specified range does not overflow a signed type. OpenMP versions 2.0 and 2.5 allow for signed integral index types only. OpenMP also does not validate the index range.  
  
 The version of this example that uses the Concurrency Runtime also uses a [concurrency::combinable](../vs140/combinable-Class.md) object in place of the [atomic](../vs140/atomic.md) directive to increment the counter value without requiring synchronization.  
  
 For more information about `parallel_for` and other parallel algorithms, see [Parallel Algorithms](../vs140/Parallel-Algorithms.md). For more information about the `combinable` class, see [Parallel Containers and Objects](../vs140/Parallel-Containers-and-Objects.md).  
  
## Example  
 This example modifies the previous one to act on an [std::array](../vs140/array-Class--STL-.md) object instead of on a native array. Because OpenMP versions 2.0 and 2.5 allow for signed integral index types only in a `parallel``for` construct, you cannot use iterators to access the elements of a Standard Template Library (STL) container in parallel. The Parallel Patterns Library (PPL) provides the [concurrency::parallel_for_each](../vs140/parallel_for_each-Function.md) algorithm, which performs tasks, in parallel, on an iterative container such as those provided by the STL. It uses the same partitioning logic that the `parallel_for` algorithm uses. The `parallel_for_each` algorithm resembles the STL [std::for_each](../vs140/for_each.md) algorithm, except that the `parallel_for_each` algorithm executes the tasks concurrently.  
  
 [!CODE [concrt-openmp#10](../CodeSnippet/VS_Snippets_ConcRT/concrt-openmp#10)]  
  
## Compiling the Code  
 Copy the example code and paste it in a Visual Studio project, or paste it in a file that is named `concrt-omp-count-primes.cpp` and then run the following command in a Visual Studio Command Prompt window.  
  
 **cl.exe /EHsc /openmp concrt-omp-count-primes.cpp**  
  
## See Also  
 [Migrating from OpenMP to the Concurrency Runtime](../vs140/Migrating-from-OpenMP-to-the-Concurrency-Runtime.md)   
 [Parallel Algorithms](../vs140/Parallel-Algorithms.md)   
 [Parallel Containers and Objects](../vs140/Parallel-Containers-and-Objects.md)