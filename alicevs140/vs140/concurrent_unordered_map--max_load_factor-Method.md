---
title: "concurrent_unordered_map::max_load_factor Method"
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
ms.assetid: 53cdec5e-f78b-4a76-8353-dac23518329f
caps.latest.revision: 6
translation.priority.ht: 
  - de-de
  - ja-jp
---
# concurrent_unordered_map::max_load_factor Method
Gets or sets the maximum load factor of the container. The maximum load factor is the largest number of elements than can be in any bucket before the container grows its internal table.  
  
## Syntax  
  
```  
float max_load_factor( ) const;  
void max_load_factor(  
   float _Newmax  
);  
```  
  
#### Parameters  
 `_Newmax`  
  
## Return Value  
 The first member function returns the stored maximum load factor. The second member function does not return a value but throws an [out_of_range](../vs140/out_of_range-Class.md) exception if the supplied load factor is invalid..  
  
## Requirements  
 **Header:** internal_concurrent_hash.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [concurrent_unordered_map Class](../vs140/concurrent_unordered_map-Class.md)