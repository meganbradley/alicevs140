---
title: "multitype_join::release Method"
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
ms.assetid: 009a4fec-f0ef-4de3-976f-eab6b357ca65
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# multitype_join::release Method
Releases a previous successful message reservation.  
  
## Syntax  
  
```  
virtual void release(  
   runtime_object_identity _MsgId,  
   _Inout_ ITarget<_Destination_type> * _PTarget  
);  
```  
  
#### Parameters  
 `_MsgId`  
 The `runtime_object_identity` of the `message` object being released.  
  
 `_PTarget`  
 A pointer to the target block that is calling the `release` method.  
  
## Requirements  
 **Header:** agents.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [multitype_join Class](../vs140/multitype_join-Class.md)