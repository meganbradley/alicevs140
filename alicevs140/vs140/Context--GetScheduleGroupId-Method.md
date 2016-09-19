---
title: "Context::GetScheduleGroupId Method"
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
ms.assetid: 433a5c65-8015-4249-9d21-4d9f96f8a4d0
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Context::GetScheduleGroupId Method
Returns an identifier for the schedule group that the context is currently working on.  
  
## Syntax  
  
```  
virtual unsigned int GetScheduleGroupId() const =0;  
```  
  
## Return Value  
 An identifier for the schedule group the context is currently working on.  
  
## Remarks  
 The return value from this method is an instantaneous sampling of the schedule group that the context is executing on. If this method is called on a context other than the current context, the value can be stale the moment it is returned and cannot be relied upon. Typically, this method is used for debugging or tracing purposes only.  
  
## Requirements  
 **Header:** concrt.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [Context Class](../vs140/Context-Class.md)   
 [ScheduleGroup Class](../vs140/ScheduleGroup-Class.md)