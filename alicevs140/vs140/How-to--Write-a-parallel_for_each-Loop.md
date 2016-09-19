---
title: "How to: Write a parallel_for_each Loop"
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
ms.assetid: fa9c0ba6-ace0-4f88-8681-c7c1f52aff20
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Write a parallel_for_each Loop
This example shows how to use the [concurrency::parallel_for_each](../vs140/parallel_for_each-Function.md) algorithm to compute the count of prime numbers in a [std::array](../vs140/array-Class--STL-.md) object in parallel.  
  
## Example  
 The following example computes the count of prime numbers in an array two times. The example first uses the [std::for_each](../vs140/for_each.md) algorithm to compute the count serially. The example then uses the `parallel_for_each` algorithm to perform the same task in parallel. The example also prints to the console the time that is required to perform both computations.  
  
 [!CODE [concrt-parallel-count-primes#1](../CodeSnippet/VS_Snippets_ConcRT/concrt-parallel-count-primes#1)]  
  
 The following sample output is for a computer that has four processors.  
  
 **serial version:**  
**found 17984 prime numbers**  
**took 6115 ms**  
**parallel version:**  
**found 17984 prime numbers**  
**took 1653 ms**   
## Compiling the Code  
 To compile the code, copy it and then paste it in a Visual Studio project, or paste it in a file that is named `parallel-count-primes.cpp` and then run the following command in a Visual Studio Command Prompt window.  
  
 **cl.exe /EHsc parallel-count-primes.cpp**  
  
## Robust Programming  
 The lambda expression that the example passes to the `parallel_for_each` algorithm uses the `InterlockedIncrement` function to enable parallel iterations of the loop to increment the counter simultaneously. If you use functions such as `InterlockedIncrement` to synchronize access to shared resources, you can present performance bottlenecks in your code. You can use a lock-free synchronization mechanism, for example, the [concurrency::combinable](../vs140/combinable-Class.md) class, to eliminate simultaneous access to shared resources. For an example that uses the `combinable` class in this manner, see [How to: Use combinable to Improve Performance](../vs140/How-to--Use-combinable-to-Improve-Performance.md).  
  
## See Also  
 [Parallel Algorithms](../vs140/Parallel-Algorithms.md)   
 [parallel_for_each Function](../vs140/parallel_for_each-Function.md)