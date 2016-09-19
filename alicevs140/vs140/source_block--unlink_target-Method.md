---
title: "source_block::unlink_target Method"
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
ms.assetid: cf6d3f9f-bef3-4af4-a543-4d8b86fbe274
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# source_block::unlink_target Method
Unlinks a target block from this `source_block` object.  
  
## Syntax  
  
```  
virtual void unlink_target(  
   _Inout_ ITarget<_Target_type> * _PTarget  
);  
```  
  
#### Parameters  
 `_PTarget`  
 A pointer to an `ITarget` block to unlink from this `source_block` object.  
  
## Remarks  
 The method throws an [invalid_argument](../vs140/invalid_argument-Class.md) exception if the parameter `_PTarget` is `NULL`.  
  
## Requirements  
 **Header:** agents.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [source_block Class](../vs140/source_block-Class.md)