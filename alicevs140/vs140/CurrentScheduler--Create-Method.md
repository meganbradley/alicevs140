---
title: "CurrentScheduler::Create Method"
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
ms.assetid: 3cce2755-d7af-4613-ba11-6783e9bf0a62
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CurrentScheduler::Create Method
Creates a new scheduler whose behavior is described by the `_Policy` parameter and attaches it to the calling context. The newly created scheduler will become the current scheduler for the calling context.  
  
## Syntax  
  
```  
static void __cdecl Create(  
   const SchedulerPolicy& _Policy  
);  
```  
  
#### Parameters  
 `_Policy`  
 The scheduler policy that describes the behavior of the newly created scheduler.  
  
## Remarks  
 The attachment of the scheduler to the calling context implicitly places a reference count on the scheduler.  
  
 After a scheduler is created with the `Create` method, you must call the [CurrentScheduler::Detach](../vs140/CurrentScheduler--Detach-Method.md) method at some point in the future in order to allow the scheduler to shut down.  
  
 If this method is called from a context that is already attached to a different scheduler, the existing scheduler is remembered as the previous scheduler, and the newly created scheduler becomes the current scheduler. When you call the `CurrentScheduler::Detach` method at a later point, the previous scheduler is restored as the current scheduler.  
  
 This method can throw a variety of exceptions, including [scheduler_resource_allocation_error](../vs140/scheduler_resource_allocation_error-Class.md) and [invalid_scheduler_policy_value](../vs140/invalid_scheduler_policy_value-Class.md).  
  
## Requirements  
 **Header:** concrt.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [CurrentScheduler Class](../vs140/CurrentScheduler-Class.md)   
 [SchedulerPolicy Class](../vs140/SchedulerPolicy-Class.md)   
 [CurrentScheduler::Detach Method](../vs140/CurrentScheduler--Detach-Method.md)   
 [Scheduler::Reference Method](../vs140/Scheduler--Reference-Method.md)   
 [Scheduler::Release Method](../vs140/Scheduler--Release-Method.md)   
 [Task Scheduler (Concurrency Runtime)](../vs140/Task-Scheduler--Concurrency-Runtime-.md)