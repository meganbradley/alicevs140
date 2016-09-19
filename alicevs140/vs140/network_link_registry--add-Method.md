---
title: "network_link_registry::add Method"
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
ms.assetid: 4da46eda-b6b2-442a-9e3e-c7eeab7a157e
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# network_link_registry::add Method
When overridden in a derived class, adds a link to the `network_link_registry` object.  
  
## Syntax  
  
```  
virtual void add(  
   _EType _Link  
) = 0;  
```  
  
#### Parameters  
 `_Link`  
 A pointer to a block to be added.  
  
## Requirements  
 **Header:** agents.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [network_link_registry Class](../vs140/network_link_registry-Class.md)