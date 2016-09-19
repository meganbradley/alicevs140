---
title: "multi_link_registry::contains Method"
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
ms.assetid: 19adc95c-4319-4d06-8b74-526ce096043e
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# multi_link_registry::contains Method
Searches the `multi_link_registry` object for a specified block.  
  
## Syntax  
  
```  
virtual bool contains(  
   _EType _Link  
);  
```  
  
#### Parameters  
 `_Link`  
 A pointer to a block that is to be searched for in the `multi_link_registry` object.  
  
## Return Value  
 `true` if the specified block was found, `false` otherwise.  
  
## Requirements  
 **Header:** agents.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [multi_link_registry Class](../vs140/multi_link_registry-Class.md)