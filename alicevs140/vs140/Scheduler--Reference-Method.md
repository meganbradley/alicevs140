---
title: "Scheduler::Reference Method"
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
ms.assetid: 46fc6f42-48e2-4274-b34d-99c44179fa16
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Scheduler::Reference Method
Increments the scheduler reference count.  
  
## Syntax  
  
```  
virtual unsigned int Reference() =0 ;  
```  
  
## Return Value  
 The newly incremented reference count.  
  
## Remarks  
 This is typically used to manage the lifetime of the scheduler for composition. When the reference count of a scheduler falls to zero, the scheduler will shut down and destruct itself after all work on the scheduler has completed.  
  
 The method will throw an [improper_scheduler_reference](../vs140/improper_scheduler_reference-Class.md) exception if the reference count prior to calling the `Reference` method was zero and the call is made from a context that is not owned by the scheduler.  
  
## Requirements  
 **Header:** concrt.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [Scheduler Class](../vs140/Scheduler-Class.md)   
 [Scheduler::Release Method](../vs140/Scheduler--Release-Method.md)   
 [Scheduler::Create Method](../vs140/Scheduler--Create-Method.md)