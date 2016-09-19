---
title: "overwrite_buffer::link_target_notification Method"
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
ms.assetid: 318132a1-e892-41db-9f66-2dc971666438
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# overwrite_buffer::link_target_notification Method
A callback that notifies that a new target has been linked to this `overwrite_buffer` messaging block.  
  
## Syntax  
  
```  
virtual void link_target_notification(  
   _Inout_ ITarget<_Type> * _PTarget  
);  
```  
  
#### Parameters  
 `_PTarget`  
 A pointer to the newly linked target.  
  
## Requirements  
 **Header:** agents.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [overwrite_buffer Class](../vs140/overwrite_buffer-Class.md)