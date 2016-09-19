---
title: "concurrent_unordered_multiset::load_factor Method"
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
ms.assetid: 66cd8c0e-516d-4f90-bdbf-761472ed7d5b
caps.latest.revision: 6
translation.priority.ht: 
  - de-de
  - ja-jp
---
# concurrent_unordered_multiset::load_factor Method
Computes and returns the current load factor of the container. The load factor is the number of elements in the container divided by the number of buckets.  
  
## Syntax  
  
```  
float load_factor() const;  
```  
  
## Return Value  
 The load factor for the container.  
  
## Requirements  
 **Header:** internal_concurrent_hash.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [concurrent_unordered_multiset Class](../vs140/concurrent_unordered_multiset-Class.md)