---
title: "invalid_scheduler_policy_key Class"
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
ms.assetid: 6a7c42fe-9bc4-4a02-bebb-99fe9ef9817d
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# invalid_scheduler_policy_key Class
This class describes an exception thrown when an invalid or unknown key is passed to a             `SchedulerPolicy` object constructor, or the             `SetPolicyValue` method of a             `SchedulerPolicy` object is passed a key that must be changed using other means such as the             `SetConcurrencyLimits` method.  
  
## Syntax  
  
```  
class invalid_scheduler_policy_key : public std::exception;  
```  
  
## Members  
  
### Public Constructors  
  
|Name|Description|  
|----------|-----------------|  
|[invalid_scheduler_policy_key::invalid_scheduler_policy_key Constructor](#invalid_scheduler_policy_key__invalid_scheduler_policy_key_constructor)|Overloaded. Constructs an                                         `invalid_scheduler_policy_key` object.|  
  
## Inheritance Hierarchy  
 `exception`  
  
 `invalid_scheduler_policy_key`  
  
## Requirements  
 **Header:** concrt.h  
  
 **Namespace:** concurrency  
  
##  <a name="invalid_scheduler_policy_key__invalid_scheduler_policy_key_constructor"></a>  invalid_scheduler_policy_key::invalid_scheduler_policy_key Constructor  
 Constructs an                 `invalid_scheduler_policy_key` object.  
  
```  
explicit _CRTIMP invalid_scheduler_policy_key(  
   _In_z_ const char *                 _Message  
) throw();  
  
invalid_scheduler_policy_key() throw();  
```  
  
### Parameters  
 `_Message`  
 A descriptive message of the error.  
  
## See Also  
 [concurrency Namespace](../vs140/concurrency-Namespace.md)   
 [SchedulerPolicy Class](../vs140/SchedulerPolicy-Class.md)   
 [PolicyElementKey Enumeration](concurrency_namespace_Enumerations)   
 [SchedulerPolicy::SetPolicyValue Method](../vs140/SchedulerPolicy-Class.md#schedulerpolicy__setpolicyvalue_method)   
 [SchedulerPolicy::SetConcurrencyLimits Method](../vs140/SchedulerPolicy-Class.md#schedulerpolicy__setconcurrencylimits_method)