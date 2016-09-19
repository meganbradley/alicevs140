---
title: "Context::ScheduleGroupId Method"
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
ms.assetid: 7583b14e-94c8-4caa-8e1b-7f97d531a3d8
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Context::ScheduleGroupId Method
Returns an identifier for the schedule group that the current context is working on.  
  
## Syntax  
  
```  
static unsigned int __cdecl ScheduleGroupId();  
```  
  
## Return Value  
 If the current context is attached to a scheduler and working on a schedule group, an identifier for the scheduler group that the current context is working on; otherwise, the value `-1`.  
  
## Requirements  
 **Header:** concrt.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [Context Class](../vs140/Context-Class.md)   
 [ScheduleGroup Class](../vs140/ScheduleGroup-Class.md)