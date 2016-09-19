---
title: "multi_link_registry::set_bound Method"
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
ms.assetid: cc5eee15-6575-48e7-89de-abdb08753020
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# multi_link_registry::set_bound Method
Sets an upper bound on the number of links that the `multi_link_registry` object can hold.  
  
## Syntax  
  
```  
void set_bound(  
   size_t _MaxLinks  
);  
```  
  
#### Parameters  
 `_MaxLinks`  
 The maximum number of links that the `multi_link_registry` object can hold.  
  
## Remarks  
 After a bound is set, unlinking an entry will cause the `multi_link_registry` object to enter an immutable state where further calls to `add` will throw an `invalid_link_target` exception.  
  
## Requirements  
 **Header:** agents.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [multi_link_registry Class](../vs140/multi_link_registry-Class.md)