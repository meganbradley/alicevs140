---
title: "SchedulerPolicy::GetPolicyValue Method"
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
ms.assetid: 84e9986a-0307-4224-aac5-10427f1e6e89
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# SchedulerPolicy::GetPolicyValue Method
Retrieves the value of the policy key supplied as the `_Key` parameter.  
  
## Syntax  
  
```  
unsigned int GetPolicyValue(  
   PolicyElementKey _Key  
) const;  
```  
  
#### Parameters  
 `_Key`  
 The policy key to retrieve a value for.  
  
## Return Value  
 If the key specified by the `_Key` parameter is supported, the policy value for the key cast to an `unsigned int`.  
  
## Remarks  
 The method will throw [invalid_scheduler_policy_key](../vs140/invalid_scheduler_policy_key-Class.md) for an invalid policy key.  
  
## Requirements  
 **Header:** concrt.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [SchedulerPolicy Class](../vs140/SchedulerPolicy-Class.md)   
 [SchedulerPolicy::SetPolicyValue Method](../vs140/SchedulerPolicy--SetPolicyValue-Method.md)   
 [SchedulerPolicy::SetConcurrencyLimits Method](../vs140/SchedulerPolicy--SetConcurrencyLimits-Method.md)   
 [PolicyElementKey Enumeration](../vs140/PolicyElementKey-Enumeration.md)