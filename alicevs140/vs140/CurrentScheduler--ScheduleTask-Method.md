---
title: "CurrentScheduler::ScheduleTask Method"
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
ms.assetid: 194110b6-182e-4d5e-8c34-11763f9fd3d7
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CurrentScheduler::ScheduleTask Method
Schedules a light-weight task within the scheduler associated with the calling context. The light-weight task will be placed in a schedule group determined by the runtime. The version that takes the parameter `_Placement` causes the task to be biased towards executing at the specified location.  
  
## Syntax  
  
```  
static void __cdecl ScheduleTask(  
   TaskProc _Proc,  
   _Inout_opt_ void * _Data  
);  
  
static void __cdecl ScheduleTask(  
   TaskProc _Proc,  
   _Inout_opt_ void * _Data,  
   location& _Placement  
);  
```  
  
#### Parameters  
 `_Proc`  
 A pointer to the function to execute to perform the body of the light-weight task.  
  
 `_Data`  
 A void pointer to the data that will be passed as a parameter to the body of the task.  
  
 `_Placement`  
 A reference to a location where the light-weight task will be biased towards executing at.  
  
## Remarks  
 This method will result in the process' default scheduler being created and/or attached to the calling context if there is no scheduler currently associated with the calling context.  
  
## Requirements  
 **Header:** concrt.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [CurrentScheduler Class](../vs140/CurrentScheduler-Class.md)   
 [Task Scheduler (Concurrency Runtime)](../vs140/Task-Scheduler--Concurrency-Runtime-.md)   
 [ScheduleGroup Class](../vs140/ScheduleGroup-Class.md)   
 [location Class](../vs140/location-Class.md)