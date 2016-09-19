---
title: "multi_link_registry::add Method"
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
ms.assetid: d73dccf7-b650-461d-9fc2-31228b28749f
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# multi_link_registry::add Method
Adds a link to the `multi_link_registry` object.  
  
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
 The method throws an [invalid_link_target](../vs140/invalid_link_target-Class.md) exception if the link is already present in the registry, or if a bound has already been set with the `set_bound` function and a link has since been removed.  
  
## Requirements  
 **Header:** agents.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [multi_link_registry Class](../vs140/multi_link_registry-Class.md)