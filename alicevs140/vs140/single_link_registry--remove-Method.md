---
title: "single_link_registry::remove Method"
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
ms.assetid: 0bccdc52-1e29-4d17-bd5d-b23e4128dd83
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# single_link_registry::remove Method
Removes a link from the `single_link_registry` object.  
  
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
 [single_link_registry Class](../vs140/single_link_registry-Class.md)