---
title: "SchedulerPolicy Class"
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
ms.assetid: bcebf51a-65f8-45a3-809b-d1ff93527dc4
caps.latest.revision: 21
translation.priority.ht: 
  - de-de
  - ja-jp
---
# SchedulerPolicy Class
The             `SchedulerPolicy` class contains a set of key/value pairs, one for each policy element, that control the behavior of a scheduler instance.  
  
## Syntax  
  
```  
class SchedulerPolicy;  
```  
  
## Members  
  
### Public Constructors  
  
|Name|Description|  
|----------|-----------------|  
|[SchedulerPolicy::SchedulerPolicy Constructor](#schedulerpolicy__schedulerpolicy_constructor)|Overloaded. Constructs a new scheduler policy and populates it with values for                                         [policy keys](concurrency_namespace_Enumerations) supported by Concurrency Runtime schedulers and the Resource Manager.|  
|[SchedulerPolicy::~SchedulerPolicy Destructor](#schedulerpolicy___dtorschedulerpolicy_destructor)|Destroys a scheduler policy.|  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[SchedulerPolicy::GetPolicyValue Method](#schedulerpolicy__getpolicyvalue_method)|Retrieves the value of the policy key supplied as the                                         `_Key` parameter.|  
|[SchedulerPolicy::SetConcurrencyLimits Method](#schedulerpolicy__setconcurrencylimits_method)|Simultaneously sets the                                         `MinConcurrency` and                                         `MaxConcurrency` policies on the                                         `SchedulerPolicy` object.|  
|[SchedulerPolicy::SetPolicyValue Method](#schedulerpolicy__setpolicyvalue_method)|Sets the value of the policy key supplied as the                                         `_Key` parameter and returns the old value.|  
  
### Public Operators  
  
|Name|Description|  
|----------|-----------------|  
|[SchedulerPolicy::operator= Operator](#schedulerpolicy__operator_eq_operator)|Assigns the scheduler policy from another scheduler policy.|  
  
## Remarks  
 For more information about the policies which can be controlled using the                 `SchedulerPolicy` class, see                 [PolicyElementKey Enumeration](concurrency_namespace_Enumerations).  
  
## Inheritance Hierarchy  
 `SchedulerPolicy`  
  
## Requirements  
 **Header:** concrt.h, concrtrm.h  
  
 **Namespace:** concurrency  
  
##  <a name="schedulerpolicy__getpolicyvalue_method"></a>  SchedulerPolicy::GetPolicyValue Method  
 Retrieves the value of the policy key supplied as the                 `_Key` parameter.  
  
```  
unsigned int GetPolicyValue(  
   PolicyElementKey                 _Key  
) const;  
```  
  
### Parameters  
 `_Key`  
 The policy key to retrieve a value for.  
  
### Return Value  
 If the key specified by the                         `_Key` parameter is supported, the policy value for the key cast to an                         `unsigned int`.  
  
### Remarks  
 The method will throw                         [invalid_scheduler_policy_key](../vs140/invalid_scheduler_policy_key-Class.md) for an invalid policy key.  
  
##  <a name="schedulerpolicy__operator_eq_operator"></a>  SchedulerPolicy::operator= Operator  
 Assigns the scheduler policy from another scheduler policy.  
  
```  
SchedulerPolicy& operator=(  
   const SchedulerPolicy&                 _RhsPolicy  
);  
```  
  
### Parameters  
 `_RhsPolicy`  
 The policy to assign to this policy.  
  
### Return Value  
 A reference to the scheduler policy.  
  
### Remarks  
 Often, the most convenient way to define a new scheduler policy is to copy an existing policy and modify it using the                         `SetPolicyValue` or                         `SetConcurrencyLimits` methods.  
  
##  <a name="schedulerpolicy__schedulerpolicy_constructor"></a>  SchedulerPolicy::SchedulerPolicy Constructor  
 Constructs a new scheduler policy and populates it with values for                 [policy keys](concurrency_namespace_Enumerations) supported by Concurrency Runtime schedulers and the Resource Manager.  
  
```  
SchedulerPolicy();  
  
SchedulerPolicy(  
   size_t                 _PolicyKeyCount,  
   ...  
);  
  
SchedulerPolicy(  
   const SchedulerPolicy&                 _SrcPolicy  
);  
```  
  
### Parameters  
 `_PolicyKeyCount`  
 The number of key/value pairs that follow the                                 `_PolicyKeyCount` parameter.  
  
 `_SrcPolicy`  
 The source policy to copy.  
  
### Remarks  
 The first constructor creates a new scheduler policy where all policies will be initialized to their default values.  
  
 The second constructor creates a new scheduler policy that uses a named-parameter style of initialization. Values after the                         `_PolicyKeyCount` parameter are supplied as key/value pairs. Any policy key which is not specified in this constructor will have its default value. This constructor could throw the exceptions                         [invalid_scheduler_policy_key](../vs140/invalid_scheduler_policy_key-Class.md),                         [invalid_scheduler_policy_value](../vs140/invalid_scheduler_policy_value-Class.md) or                         [invalid_scheduler_policy_thread_specification](../vs140/invalid_scheduler_policy_thread_specification-Class.md).  
  
 The third constructor is a copy constructor. Often, the most convenient way to define a new scheduler policy is to copy an existing policy and modify it using the                         `SetPolicyValue` or                         `SetConcurrencyLimits` methods.  
  
##  <a name="schedulerpolicy___dtorschedulerpolicy_destructor"></a>  SchedulerPolicy::~SchedulerPolicy Destructor  
 Destroys a scheduler policy.  
  
```  
~SchedulerPolicy();  
```  
  
##  <a name="schedulerpolicy__setconcurrencylimits_method"></a>  SchedulerPolicy::SetConcurrencyLimits Method  
 Simultaneously sets the                 `MinConcurrency` and                 `MaxConcurrency` policies on the                 `SchedulerPolicy` object.  
  
```  
void SetConcurrencyLimits(  
   unsigned int                 _MinConcurrency,  
   unsigned int                 _MaxConcurrency = MaxExecutionResources  
);  
```  
  
### Parameters  
 `_MinConcurrency`  
 The value for the                                 `MinConcurrency` policy key.  
  
 `_MaxConcurrency`  
 The value for the                                 `MaxConcurrency` policy key.  
  
### Remarks  
 The method will throw                         [invalid_scheduler_policy_thread_specification](../vs140/invalid_scheduler_policy_thread_specification-Class.md) if the value specified for the                         `MinConcurrency` policy is greater than that specified for the                         `MaxConcurrency` policy.  
  
 The method can also throw                         [invalid_scheduler_policy_value](../vs140/invalid_scheduler_policy_value-Class.md) for other invalid values.  
  
##  <a name="schedulerpolicy__setpolicyvalue_method"></a>  SchedulerPolicy::SetPolicyValue Method  
 Sets the value of the policy key supplied as the                 `_Key` parameter and returns the old value.  
  
```  
unsigned int SetPolicyValue(  
   PolicyElementKey                 _Key,  
   unsigned int                 _Value  
);  
```  
  
### Parameters  
 `_Key`  
 The policy key to set a value for.  
  
 `_Value`  
 The value to set the policy key to.  
  
### Return Value  
 If the key specified by the                         `_Key` parameter is supported, the old policy value for the key cast to an                         `unsigned int`.  
  
### Remarks  
 The method will throw                         [invalid_scheduler_policy_key](../vs140/invalid_scheduler_policy_key-Class.md) for an invalid policy key or any policy key whose value cannot be set by the                         `SetPolicyValue` method.  
  
 The method will throw                         [invalid_scheduler_policy_value](../vs140/invalid_scheduler_policy_value-Class.md) for a value that is not supported for the key specified by the                         `_Key` parameter.  
  
 Note that this method is not allowed to set the                         `MinConcurrency` or                         `MaxConcurrency` policies. To set these values, use the                         [SetConcurrencyLimits](#schedulerpolicy__setconcurrencylimits_method) method.  
  
## See Also  
 [concurrency Namespace](../vs140/concurrency-Namespace.md)   
 [PolicyElementKey Enumeration](concurrency_namespace_Enumerations)   
 [CurrentScheduler Class](../vs140/CurrentScheduler-Class.md)   
 [Scheduler Class](../vs140/Scheduler-Class.md)   
 [Task Scheduler (Concurrency Runtime)](../vs140/Task-Scheduler--Concurrency-Runtime-.md)