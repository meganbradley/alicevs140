---
title: "multi_link_registry::remove Method"
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
ms.assetid: ce3c86d3-13c4-46c8-91ce-e523a3cd5561
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# multi_link_registry::remove Method
Removes a link from the `multi_link_registry` object.  
  
## Syntax  
  
```  
virtual bool remove(  
   _EType _Link  
);  
```  
  
#### Parameters  
 `_Link`  
 A pointer to a block to be removed, if found.  
  
## Return Value  
 `true` if the link was found and removed, `false` otherwise.  
  
## Requirements  
 **Header:** agents.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [multi_link_registry Class](../vs140/multi_link_registry-Class.md)