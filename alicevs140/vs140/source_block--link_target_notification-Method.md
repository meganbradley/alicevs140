---
title: "source_block::link_target_notification Method"
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
ms.assetid: b3e07aed-cf3a-4389-94ea-2074b3d30b2a
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# source_block::link_target_notification Method
A callback that notifies that a new target has been linked to this `source_block` object.  
  
## Syntax  
  
```  
virtual void link_target_notification(  
   _Inout_ ITarget<_Target_type> *  
);  
```  
  
## Requirements  
 **Header:** agents.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [source_block Class](../vs140/source_block-Class.md)