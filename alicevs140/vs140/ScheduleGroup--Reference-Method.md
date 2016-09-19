---
title: "ScheduleGroup::Reference Method"
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
ms.assetid: df0182d7-1fdd-4b1f-b4a8-9852aead7fe5
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ScheduleGroup::Reference Method
Increments the schedule group reference count.  
  
## Syntax  
  
```  
virtual unsigned int Reference() =0;  
```  
  
## Return Value  
 The newly incremented reference count.  
  
## Remarks  
 This is typically used to manage the lifetime of the schedule group for composition. When the reference count of a schedule group falls to zero, the schedule group is deleted by the runtime. A schedule group created using either the [CurrentScheduler::CreateScheduleGroup](../vs140/CurrentScheduler--CreateScheduleGroup-Method.md) method, or the [Scheduler::CreateScheduleGroup](../vs140/Scheduler--CreateScheduleGroup-Method.md) method starts out with a reference count of one.  
  
## Requirements  
 **Header:** concrt.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [ScheduleGroup Class](../vs140/ScheduleGroup-Class.md)   
 [ScheduleGroup::Release Method](../vs140/ScheduleGroup--Release-Method.md)   
 [CurrentScheduler::CreateScheduleGroup Method](../vs140/CurrentScheduler--CreateScheduleGroup-Method.md)   
 [Scheduler::CreateScheduleGroup Method](../vs140/Scheduler--CreateScheduleGroup-Method.md)