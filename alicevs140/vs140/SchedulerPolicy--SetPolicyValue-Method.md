---
title: "SchedulerPolicy::SetPolicyValue Method"
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
ms.assetid: bc74de7d-e564-4d9c-aa16-c71bc61470c5
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# SchedulerPolicy::SetPolicyValue Method
Sets the value of the policy key supplied as the `_Key` parameter and returns the old value.  
  
## Syntax  
  
```  
unsigned int SetPolicyValue(  
   PolicyElementKey _Key,  
   unsigned int _Value  
);  
```  
  
#### Parameters  
 `_Key`  
 The policy key to set a value for.  
  
 `_Value`  
 The value to set the policy key to.  
  
## Return Value  
 If the key specified by the `_Key` parameter is supported, the old policy value for the key cast to an `unsigned int`.  
  
## Remarks  
 The method will throw [invalid_scheduler_policy_key](../vs140/invalid_scheduler_policy_key-Class.md) for an invalid policy key or any policy key whose value cannot be set by the `SetPolicyValue` method.  
  
 The method will throw [invalid_scheduler_policy_value](../vs140/invalid_scheduler_policy_value-Class.md) for a value that is not supported for the key specified by the `_Key` parameter.  
  
 Note that this method is not allowed to set the `MinConcurrency` or `MaxConcurrency` policies. To set these values, use the [SetConcurrencyLimits](../vs140/SchedulerPolicy--SetConcurrencyLimits-Method.md) method.  
  
## Requirements  
 **Header:** concrt.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [SchedulerPolicy Class](../vs140/SchedulerPolicy-Class.md)   
 [SchedulerPolicy::GetPolicyValue Method](../vs140/SchedulerPolicy--GetPolicyValue-Method.md)   
 [SchedulerPolicy::SetConcurrencyLimits Method](../vs140/SchedulerPolicy--SetConcurrencyLimits-Method.md)   
 [PolicyElementKey Enumeration](../vs140/PolicyElementKey-Enumeration.md)