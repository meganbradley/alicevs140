---
title: "concurrent_vector::rend Method"
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
ms.assetid: 6582437f-942f-4fa7-bad6-60de775afb1e
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# concurrent_vector::rend Method
Returns an iterator of type `reverse_iterator` or `const_reverse_iterator` to the end of the concurrent vector. This method is concurrency-safe.  
  
## Syntax  
  
```  
reverse_iterator rend();  
  
const_reverse_iterator rend() const;  
```  
  
## Return Value  
 An iterator of type `reverse_iterator` or `const_reverse_iterator` to the end of the concurrent vector.  
  
## Requirements  
 **Header:** concurrent_vector.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [concurrent_vector Class](../vs140/concurrent_vector-Class.md)