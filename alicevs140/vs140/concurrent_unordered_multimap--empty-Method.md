---
title: "concurrent_unordered_multimap::empty Method"
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
ms.assetid: c9f3c0e6-d092-445f-bc6f-9f890865a072
caps.latest.revision: 6
translation.priority.ht: 
  - de-de
  - ja-jp
---
# concurrent_unordered_multimap::empty Method
Tests whether no elements are present. This method is concurrency safe.  
  
## Syntax  
  
```  
bool empty() const;  
```  
  
## Return Value  
 `true` if the concurrent container is empty, `false` otherwise.  
  
## Remarks  
 In the presence of concurrent inserts, whether or not the concurrent container is empty may change immediately after calling this function, before the return value is even read.  
  
## Requirements  
 **Header:** internal_concurrent_hash.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [concurrent_unordered_multimap Class](../vs140/concurrent_unordered_multimap-Class.md)