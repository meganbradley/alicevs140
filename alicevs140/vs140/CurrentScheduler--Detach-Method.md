---
title: "CurrentScheduler::Detach Method"
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
ms.assetid: edba8811-cfd5-4209-9ae0-874afeca393b
caps.latest.revision: 21
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CurrentScheduler::Detach Method
Detaches the current scheduler from the calling context and restores the previously attached scheduler as the current scheduler, if one exists. After this method returns, the calling context is then managed by the scheduler that was previously attached to the context using either the `CurrentScheduler::Create` or `Scheduler::Attach` method.  
  
## Syntax  
  
```  
static void __cdecl Detach();  
```  
  
## Remarks  
 The `Detach` method implicitly removes a reference count from the scheduler.  
  
 If there is no scheduler attached to the calling context, calling this method will result in a [scheduler_not_attached](../vs140/scheduler_not_attached-Class.md) exception being thrown.  
  
 Calling this method from a context that is internal to and managed by a scheduler, or a context that was attached using a method other than the [Scheduler::Attach](../vs140/Scheduler--Attach-Method.md) or [CurrentScheduler::Create](../vs140/CurrentScheduler--Create-Method.md) methods, will result in an [improper_scheduler_detach](../vs140/improper_scheduler_detach-Class.md) exception being thrown.  
  
## Requirements  
 **Header:** concrt.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [CurrentScheduler Class](../vs140/CurrentScheduler-Class.md)   
 [Scheduler::Attach Method](../vs140/Scheduler--Attach-Method.md)   
 [CurrentScheduler::Create Method](../vs140/CurrentScheduler--Create-Method.md)