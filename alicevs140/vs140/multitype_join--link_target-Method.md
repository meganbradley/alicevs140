---
title: "multitype_join::link_target Method"
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
ms.assetid: abdfb95d-6c19-4889-90b4-af28e0ad21aa
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# multitype_join::link_target Method
Links a target block to this `multitype_join` messaging block.  
  
## Syntax  
  
```  
virtual void link_target(  
   _Inout_ ITarget<_Destination_type> * _PTarget  
);  
```  
  
#### Parameters  
 `_PTarget`  
 A pointer to an `ITarget` block to link to this `multitype_join` messaging block.  
  
## Requirements  
 **Header:** agents.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [multitype_join Class](../vs140/multitype_join-Class.md)