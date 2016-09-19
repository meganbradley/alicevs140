---
title: "ScheduleGroup::Release Method"
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
ms.assetid: 8f60d3af-c43f-48a5-9eb3-37ad398f1787
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ScheduleGroup::Release Method
Decrements the scheduler group reference count.  
  
## Syntax  
  
```  
virtual unsigned int Release() =0;  
```  
  
## Return Value  
 The newly decremented reference count.  
  
## Remarks  
 This is typically used to manage the lifetime of the schedule group for composition. When the reference count of a schedule group falls to zero, the schedule group is deleted by the runtime. After you have called the `Release` method the specific number of times to remove the creation reference count and any additional references placed using the `Reference` method, you cannot utilize the schedule group further. Doing so will result in undefined behavior.  
  
 A schedule group is associated with a particular scheduler instance. You must ensure that all references to the schedule group are released before all references to the scheduler are released, because the latter could result in the scheduler being destroyed. Doing otherwise results in undefined behavior.  
  
## Requirements  
 **Header:** concrt.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [ScheduleGroup Class](../vs140/ScheduleGroup-Class.md)   
 [ScheduleGroup::Reference Method](../vs140/ScheduleGroup--Reference-Method.md)   
 [CurrentScheduler::CreateScheduleGroup Method](../vs140/CurrentScheduler--CreateScheduleGroup-Method.md)   
 [Scheduler::CreateScheduleGroup Method](../vs140/Scheduler--CreateScheduleGroup-Method.md)