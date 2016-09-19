---
title: "single_link_registry::add Method"
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
ms.assetid: ccafd9a9-1cf3-4754-b357-6e2ee4d14f40
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# single_link_registry::add Method
Adds a link to the `single_link_registry` object.  
  
## Syntax  
  
```  
virtual void add(  
   _EType _Link  
);  
```  
  
#### Parameters  
 `_Link`  
 A pointer to a block to be added.  
  
## Remarks  
 The method throws an [invalid_link_target](../vs140/invalid_link_target-Class.md) exception if there is already a link in this registry.  
  
## Requirements  
 **Header:** agents.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [single_link_registry Class](../vs140/single_link_registry-Class.md)