---
title: "Scheduler::Create Method"
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
ms.assetid: cedf71a9-e1f4-4e7e-9e01-6a2e74df65c8
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Scheduler::Create Method
Creates a new scheduler whose behavior is described by the `_Policy` parameter, places an initial reference on the scheduler, and returns a pointer to it.  
  
## Syntax  
  
```  
static Scheduler * __cdecl Create(  
   const SchedulerPolicy& _Policy  
);  
```  
  
#### Parameters  
 `_Policy`  
 The scheduler policy that describes behavior of the newly created scheduler.  
  
## Return Value  
 A pointer to a newly created scheduler. This `Scheduler` object has an initial reference count placed on it.  
  
## Remarks  
 After a scheduler is created with the `Create` method, you must call the `Release` method at some point in the future in order to remove the initial reference count and allow the scheduler to shut down.  
  
 A scheduler created with this method is not attached to the calling context. It can be attached to a context using the [Attach](../vs140/Scheduler--Attach-Method.md) method.  
  
 This method can throw a variety of exceptions, including [scheduler_resource_allocation_error](../vs140/scheduler_resource_allocation_error-Class.md) and [invalid_scheduler_policy_value](../vs140/invalid_scheduler_policy_value-Class.md).  
  
## Requirements  
 **Header:** concrt.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [Scheduler Class](../vs140/Scheduler-Class.md)   
 [Scheduler::Release Method](../vs140/Scheduler--Release-Method.md)   
 [Scheduler::Attach Method](../vs140/Scheduler--Attach-Method.md)   
 [CurrentScheduler::Create Method](../vs140/CurrentScheduler--Create-Method.md)   
 [PolicyElementKey Enumeration](../vs140/PolicyElementKey-Enumeration.md)   
 [Task Scheduler (Concurrency Runtime)](../vs140/Task-Scheduler--Concurrency-Runtime-.md)