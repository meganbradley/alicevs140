---
title: "concurrent_vector::empty Method"
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
ms.assetid: e9f9bee2-d482-44ba-9eb4-0a3205baf6c8
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# concurrent_vector::empty Method
Tests if the concurrent vector is empty at the time this method is called. This method is concurrency-safe.  
  
## Syntax  
  
```  
bool empty() const;  
```  
  
## Return Value  
 `true` if the vector was empty at the moment the function was called, `false` otherwise.  
  
## Requirements  
 **Header:** concurrent_vector.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [concurrent_vector Class](../vs140/concurrent_vector-Class.md)