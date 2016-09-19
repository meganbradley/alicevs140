---
title: "source_block::release Method"
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
ms.assetid: 6e79bb10-e268-4025-b96a-650de601aedd
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# source_block::release Method
Releases a previous successful message reservation.  
  
## Syntax  
  
```  
virtual void release(  
   runtime_object_identity _MsgId,  
   _Inout_ ITarget<_Target_type> * _PTarget  
);  
```  
  
#### Parameters  
 `_MsgId`  
 The `runtime_object_identity` of the reserved `message` object.  
  
 `_PTarget`  
 A pointer to the target block that is calling the `release` method.  
  
## Remarks  
 The method throws an [invalid_argument](../vs140/invalid_argument-Class.md) exception if the parameter `_PTarget` is `NULL`.  
  
 The method throws a [bad_target](../vs140/bad_target-Class.md) exception if the parameter `_PTarget` does not represent the target that called `reserve`.  
  
## Requirements  
 **Header:** agents.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [source_block Class](../vs140/source_block-Class.md)