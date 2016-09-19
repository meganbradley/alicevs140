---
title: "SchedulerPolicy::SetConcurrencyLimits Method"
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
ms.assetid: 829ac25b-ad8e-4901-910d-02fda8dc720d
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# SchedulerPolicy::SetConcurrencyLimits Method
Simultaneously sets the `MinConcurrency` and `MaxConcurrency` policies on the `SchedulerPolicy` object.  
  
## Syntax  
  
```  
void SetConcurrencyLimits(  
   unsigned int _MinConcurrency,  
   unsigned int _MaxConcurrency = MaxExecutionResources  
);  
```  
  
#### Parameters  
 `_MinConcurrency`  
 The value for the `MinConcurrency` policy key.  
  
 `_MaxConcurrency`  
 The value for the `MaxConcurrency` policy key.  
  
## Remarks  
 The method will throw [invalid_scheduler_policy_thread_specification](../vs140/invalid_scheduler_policy_thread_specification-Class.md) if the value specified for the `MinConcurrency` policy is greater than that specified for the `MaxConcurrency` policy.  
  
 The method can also throw [invalid_scheduler_policy_value](../vs140/invalid_scheduler_policy_value-Class.md) for other invalid values.  
  
## Requirements  
 **Header:** concrt.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [SchedulerPolicy Class](../vs140/SchedulerPolicy-Class.md)   
 [SchedulerPolicy::GetPolicyValue Method](../vs140/SchedulerPolicy--GetPolicyValue-Method.md)   
 [SchedulerPolicy::SetPolicyValue Method](../vs140/SchedulerPolicy--SetPolicyValue-Method.md)   
 [PolicyElementKey Enumeration](../vs140/PolicyElementKey-Enumeration.md)