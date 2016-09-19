---
title: "single_link_registry::contains Method"
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
ms.assetid: a3cb2cfc-08ce-4c07-9984-dfdafe422b07
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# single_link_registry::contains Method
Searches the `single_link_registry` object for a specified block.  
  
## Syntax  
  
```  
virtual bool contains(  
   _EType _Link  
);  
```  
  
#### Parameters  
 `_Link`  
 A pointer to a block that is to be searched for in the `single_link_registry` object.  
  
## Return Value  
 `true` if the link was found, `false` otherwise.  
  
## Requirements  
 **Header:** agents.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [single_link_registry Class](../vs140/single_link_registry-Class.md)