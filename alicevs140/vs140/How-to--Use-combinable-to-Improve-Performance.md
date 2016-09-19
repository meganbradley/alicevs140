---
title: "How to: Use combinable to Improve Performance"
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
ms.assetid: fa730580-1c94-4b2d-8aec-57c91dc0497e
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Use combinable to Improve Performance
This example shows how to use the [concurrency::combinable](../vs140/combinable-Class.md) class to compute the sum of the numbers in a [std::array](../vs140/array-Class--STL-.md) object that are prime. The `combinable` class improves performance by eliminating shared state.  
  
> [!TIP]
>  In some cases, parallel map ([concurrency::parallel_transform](../vs140/parallel_transform-Function.md)) and reduce ([concurrency:: parallel_reduce](../vs140/parallel_reduce-Function.md)) can provide performance improvements over `combinable`. For an example that uses map and reduce operations to produce the same results as this example, see [Parallel Algorithms](../vs140/Parallel-Algorithms.md).  
  
## Example  
 The following example uses the [std::accumulate](../vs140/accumulate.md) function to compute the sum of the elements in an array that are prime. In this example, `a` is an `array` object and the `is_prime` function determines whether its input value is prime.  
  
 [!CODE [concrt-parallel-sum-of-primes#1](../CodeSnippet/VS_Snippets_ConcRT/concrt-parallel-sum-of-primes#1)]  
  
## Example  
 The following example shows a naïve way to parallelize the previous example. This example uses the [concurrency::parallel_for_each](../vs140/parallel_for_each-Function.md) algorithm to process the array in parallel and a [concurrency::critical_section](../vs140/critical_section-Class.md) object to synchronize access to the `prime_sum` variable. This example does not scale because each thread must wait for the shared resource to become available.  
  
 [!CODE [concrt-parallel-sum-of-primes#2](../CodeSnippet/VS_Snippets_ConcRT/concrt-parallel-sum-of-primes#2)]  
  
## Example  
 The following example uses a `combinable` object to improve the performance of the previous example. This example eliminates the need for synchronization objects; it scales because the `combinable` object enables each thread to perform its task independently.  
  
 A `combinable` object is typically used in two steps. First, produce a series of fine-grained computations by performing work in parallel. Next, combine (or reduce) the computations into a final result. This example uses the [concurrency::combinable::local](../vs140/combinable--local-Method.md) method to obtain a reference to the local sum. It then uses the [concurrency::combinable::combine](../vs140/combinable--combine-Method.md) method and a [std::plus](../vs140/plus-Struct.md) object to combine the local computations into the final result.  
  
 [!CODE [concrt-parallel-sum-of-primes#3](../CodeSnippet/VS_Snippets_ConcRT/concrt-parallel-sum-of-primes#3)]  
  
## Example  
 The following complete example computes the sum of prime numbers both serially and in parallel. The example prints to the console the time that is required to perform both computations.  
  
 [!CODE [concrt-parallel-sum-of-primes#4](../CodeSnippet/VS_Snippets_ConcRT/concrt-parallel-sum-of-primes#4)]  
  
 The following sample output is for a computer that has four processors.  
  
 **1709600813**  
**serial time: 6178 ms**  
**1709600813**  
**parallel time: 1638 ms**   
## Compiling the Code  
 To compile the code, copy it and then paste it in a Visual Studio project, or paste it in a file that is named `parallel-sum-of-primes.cpp` and then run the following command in a Visual Studio Command Prompt window.  
  
 **cl.exe /EHsc parallel-sum-of-primes.cpp**  
  
## Robust Programming  
 For an example that uses map and reduce operations to produce the same results, see [Parallel Algorithms](../vs140/Parallel-Algorithms.md).  
  
## See Also  
 [Parallel Containers and Objects](../vs140/Parallel-Containers-and-Objects.md)   
 [combinable Class](../vs140/combinable-Class.md)   
 [critical_section Class](../vs140/critical_section-Class.md)