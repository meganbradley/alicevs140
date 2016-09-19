---
title: "improper_scheduler_detach Class"
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
ms.assetid: 30132102-c900-4951-a470-b63b4e3aa2d2
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# improper_scheduler_detach Class
This class describes an exception thrown when the             `CurrentScheduler::Detach` method is called on a context which has not been attached to any scheduler using the             `Attach` method of a             `Scheduler` object.  
  
## Syntax  
  
```  
class improper_scheduler_detach : public std::exception;  
```  
  
## Members  
  
### Public Constructors  
  
|Name|Description|  
|----------|-----------------|  
|[improper_scheduler_detach::improper_scheduler_detach Constructor](#improper_scheduler_detach__improper_scheduler_detach_constructor)|Overloaded. Constructs an                                         `improper_scheduler_detach` object.|  
  
## Inheritance Hierarchy  
 `exception`  
  
 `improper_scheduler_detach`  
  
## Requirements  
 **Header:** concrt.h  
  
 **Namespace:** concurrency  
  
##  <a name="improper_scheduler_detach__improper_scheduler_detach_constructor"></a>  improper_scheduler_detach::improper_scheduler_detach Constructor  
 Constructs an                 `improper_scheduler_detach` object.  
  
```  
explicit _CRTIMP improper_scheduler_detach(  
   _In_z_ const char *                 _Message  
) throw();  
  
improper_scheduler_detach() throw();  
```  
  
### Parameters  
 `_Message`  
 A descriptive message of the error.  
  
## See Also  
 [concurrency Namespace](../vs140/concurrency-Namespace.md)   
 [Scheduler Class](../vs140/Scheduler-Class.md)   
 [CurrentScheduler::Detach Method](../vs140/CurrentScheduler-Class.md#currentscheduler__detach_method)   
 [Scheduler::Attach Method](../vs140/Scheduler-Class.md#scheduler__attach_method)