---
title: "multitype_join::release_ref Method"
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
ms.assetid: 0fd6e533-c5ac-4bf1-8392-4c953349d401
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# multitype_join::release_ref Method
Releases a reference count on this `multiple_join` messaging block.  
  
## Syntax  
  
```  
virtual void release_ref(  
   _Inout_ ITarget<_Destination_type> * _PTarget  
);  
```  
  
#### Parameters  
 `_PTarget`  
 A pointer to the target block that is calling this method.  
  
## Remarks  
 This method is called by an `ITarget` object that is being unlinked from this source. The source block is allowed to release any resources reserved for the target block.  
  
## Requirements  
 **Header:** agents.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [multitype_join Class](../vs140/multitype_join-Class.md)