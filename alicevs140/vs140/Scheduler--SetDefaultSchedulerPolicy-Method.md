---
title: "Scheduler::SetDefaultSchedulerPolicy Method"
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
ms.assetid: 87bf9d4c-05ed-4b38-bbcd-1aaf541271d3
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Scheduler::SetDefaultSchedulerPolicy Method
Allows a user defined policy to be used to create the default scheduler. This method can be called only when no default scheduler exists within the process. After a default policy has been set, it remains in effect until the next valid call to either the `SetDefaultSchedulerPolicy` or the [ResetDefaultSchedulerPolicy](../vs140/Scheduler--ResetDefaultSchedulerPolicy-Method.md) method.  
  
## Syntax  
  
```  
static void __cdecl SetDefaultSchedulerPolicy(  
   const SchedulerPolicy& _Policy  
);  
```  
  
#### Parameters  
 `_Policy`  
 The policy to be set as the default scheduler policy.  
  
## Remarks  
 If the `SetDefaultSchedulerPolicy` method is called when a default scheduler already exists within the process, the runtime will throw a [default_scheduler_exists](../vs140/default_scheduler_exists-Class.md) exception.  
  
## Requirements  
 **Header:** concrt.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [Scheduler Class](../vs140/Scheduler-Class.md)   
 [Scheduler::ResetDefaultSchedulerPolicy Method](../vs140/Scheduler--ResetDefaultSchedulerPolicy-Method.md)   
 [SchedulerPolicy Class](../vs140/SchedulerPolicy-Class.md)   
 [PolicyElementKey Enumeration](../vs140/PolicyElementKey-Enumeration.md)   
 [Task Scheduler (Concurrency Runtime)](../vs140/Task-Scheduler--Concurrency-Runtime-.md)