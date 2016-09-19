---
title: "How to: Use combinable to Combine Sets"
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
ms.assetid: 66ffe8e3-6bbb-4e9f-b790-b612922a68a7
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Use combinable to Combine Sets
This topic shows how to use the [concurrency::combinable](../vs140/combinable-Class.md) class to compute the set of prime numbers.  
  
## Example  
 The following example computes the set of prime numbers two times. Each computation stores the result in a [std::bitset](../vs140/bitset-Class.md) object. The example first computes the set serially and then computes the set in parallel. The example also prints to the console the time that is required to perform both computations.  
  
 This example uses the [concurrency::parallel_for](../vs140/parallel_for-Function.md) algorithm and a `combinable` object to generate thread-local sets. It then uses the [concurrency::combinable::combine_each](../vs140/combinable--combine_each-Method.md) method to combine the thread-local sets into the final set.  
  
 [!CODE [concrt-parallel-combine-primes#1](../CodeSnippet/VS_Snippets_ConcRT/concrt-parallel-combine-primes#1)]  
  
 The following sample output is for a computer that has four processors.  
  
 **serial time: 312 ms**  
**parallel time: 78 ms**   
## Compiling the Code  
 Copy the example code and paste it in a Visual Studio project, or paste it in a file that is named `parallel-combine-primes.cpp` and then run the following command in a Visual Studio Command Prompt window.  
  
 **cl.exe /EHsc parallel-combine-primes.cpp**  
  
## See Also  
 [Parallel Containers and Objects](../vs140/Parallel-Containers-and-Objects.md)   
 [combinable Class](../vs140/combinable-Class.md)   
 [combinable::combine_each Method](../vs140/combinable--combine_each-Method.md)