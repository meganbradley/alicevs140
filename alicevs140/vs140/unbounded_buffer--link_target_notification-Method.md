---
title: "unbounded_buffer::link_target_notification Method"
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
ms.assetid: e9ceb9ba-f84a-4d93-b17e-71dd29152d7c
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# unbounded_buffer::link_target_notification Method
A callback that notifies that a new target has been linked to this `unbounded_buffer` messaging block.  
  
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
 [unbounded_buffer Class](../vs140/unbounded_buffer-Class.md)