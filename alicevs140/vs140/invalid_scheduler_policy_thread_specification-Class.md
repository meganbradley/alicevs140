---
title: "invalid_scheduler_policy_thread_specification Class"
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
ms.assetid: 2d0fafb2-18f8-4284-8040-3db640d33303
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# invalid_scheduler_policy_thread_specification Class
This class describes an exception thrown when an attempt is made to set the concurrency limits of a             `SchedulerPolicy` object such that the value of the             `MinConcurrency` key is less than the value of the             `MaxConcurrency` key.  
  
## Syntax  
  
```  
class invalid_scheduler_policy_thread_specification : public std::exception;  
```  
  
## Members  
  
### Public Constructors  
  
|Name|Description|  
|----------|-----------------|  
|[invalid_scheduler_policy_thread_specification::invalid_scheduler_policy_thread_specification Constructor](../vs140/invalid_scheduler_policy_value-Class.md#invalid_scheduler_policy_thread_specification__invalid_scheduler_policy_thread_specification_constructor)|Overloaded. Constructs an                                         `invalid_scheduler_policy_value` object.|  
  
## Inheritance Hierarchy  
 `exception`  
  
 `invalid_scheduler_policy_thread_specification`  
  
## Requirements  
 **Header:** concrt.h  
  
 **Namespace:** concurrency  
  
##  <a name="invalid_scheduler_policy_value__invalid_scheduler_policy_value_constructor"></a>  invalid_scheduler_policy_value::invalid_scheduler_policy_value Constructor  
 Constructs an                 `invalid_scheduler_policy_value` object.  
  
```  
explicit _CRTIMP invalid_scheduler_policy_value(  
   _In_z_ const char *                 _Message  
) throw();  
  
invalid_scheduler_policy_value() throw();  
```  
  
### Parameters  
 `_Message`  
 A descriptive message of the error.  
  
## See Also  
 [concurrency Namespace](../vs140/concurrency-Namespace.md)   
 [SchedulerPolicy Class](../vs140/SchedulerPolicy-Class.md)   
 [PolicyElementKey Enumeration](concurrency_namespace_Enumerations)   
 [SchedulerPolicy::SetConcurrencyLimits Method](../vs140/SchedulerPolicy-Class.md#schedulerpolicy__setconcurrencylimits_method)