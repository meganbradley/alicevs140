---
title: "SchedulerPolicy::SchedulerPolicy Constructor"
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
ms.assetid: 73ba1d7b-71f2-4a67-aaf8-8243556a64e3
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# SchedulerPolicy::SchedulerPolicy Constructor
Constructs a new scheduler policy and populates it with values for [policy keys](../vs140/PolicyElementKey-Enumeration.md) supported by Concurrency Runtime schedulers and the Resource Manager.  
  
## Syntax  
  
```  
SchedulerPolicy();  
  
SchedulerPolicy(  
   size_t _PolicyKeyCount,  
   ...  
);  
  
SchedulerPolicy(  
   const SchedulerPolicy& _SrcPolicy  
);  
```  
  
#### Parameters  
 `_PolicyKeyCount`  
 The number of key/value pairs that follow the `_PolicyKeyCount` parameter.  
  
 `_SrcPolicy`  
 The source policy to copy.  
  
## Remarks  
 The first constructor creates a new scheduler policy where all policies will be initialized to their default values.  
  
 The second constructor creates a new scheduler policy that uses a named-parameter style of initialization. Values after the `_PolicyKeyCount` parameter are supplied as key/value pairs. Any policy key which is not specified in this constructor will have its default value. This constructor could throw the exceptions [invalid_scheduler_policy_key](../vs140/invalid_scheduler_policy_key-Class.md), [invalid_scheduler_policy_value](../vs140/invalid_scheduler_policy_value-Class.md) or [invalid_scheduler_policy_thread_specification](../vs140/invalid_scheduler_policy_thread_specification-Class.md).  
  
 The third constructor is a copy constructor. Often, the most convenient way to define a new scheduler policy is to copy an existing policy and modify it using the `SetPolicyValue` or `SetConcurrencyLimits` methods.  
  
## Requirements  
 **Header:** concrt.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [SchedulerPolicy Class](../vs140/SchedulerPolicy-Class.md)   
 [SchedulerPolicy::SetPolicyValue Method](../vs140/SchedulerPolicy--SetPolicyValue-Method.md)   
 [SchedulerPolicy::GetPolicyValue Method](../vs140/SchedulerPolicy--GetPolicyValue-Method.md)   
 [SchedulerPolicy::SetConcurrencyLimits Method](../vs140/SchedulerPolicy--SetConcurrencyLimits-Method.md)   
 [PolicyElementKey Enumeration](../vs140/PolicyElementKey-Enumeration.md)