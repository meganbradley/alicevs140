---
title: "Scheduler Policies"
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
ms.assetid: 58fb68bd-4a57-40a8-807b-6edb6f083cd9
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Scheduler Policies
This document describes the role of scheduler policies in the Concurrency Runtime. A *scheduler policy* controls the strategy that the scheduler uses when it manages tasks. For example, consider an application that requires some tasks to execute at `THREAD_PRIORITY_NORMAL` and other tasks to execute at `THREAD_PRIORITY_HIGHEST`.  You can create two scheduler instances: one that specifies the `ContextPriority` policy to be `THREAD_PRIORITY_NORMAL` and another that specifies the same policy to be `THREAD_PRIORITY_HIGHEST`.  
  
 By using scheduler policies, you can divide the available processing resources and assign a fixed set of resources to each scheduler. For example, consider a parallel algorithm that does not scale beyond four processors. You can create a scheduler policy that limits its tasks to use no more than four processors concurrently.  
  
> [!TIP]
>  The Concurrency Runtime provides a default scheduler. Therefore, you don't have to create one in your application. Because the Task Scheduler helps you fine-tune the performance of your applications, we recommend that you start with the [Parallel Patterns Library (PPL)](../vs140/Parallel-Patterns-Library--PPL-.md) or the [Asynchronous Agents Library](../vs140/Asynchronous-Agents-Library.md) if you are new to the Concurrency Runtime.  
  
 When you use the [concurrency::CurrentScheduler::Create](../vs140/CurrentScheduler--Create-Method.md), [concurrency::Scheduler::Create](../vs140/Scheduler--Create-Method.md), or [concurrency::Scheduler::SetDefaultSchedulerPolicy](../vs140/Scheduler--SetDefaultSchedulerPolicy-Method.md) method to create a scheduler instance, you provide a [concurrency::SchedulerPolicy](../vs140/SchedulerPolicy-Class.md) object that contains a collection of key-value pairs that specify the behavior of the scheduler. The `SchedulerPolicy` constructor takes a variable number of arguments. The first argument is the number of policy elements that you are about to specify. The remaining arguments are key-value pairs for each policy element. The following example creates a `SchedulerPolicy` object that specifies three policy elements. The runtime uses default values for the policy keys that are not specified.  
  
 [!CODE [concrt-scheduler-policy#2](../CodeSnippet/VS_Snippets_ConcRT/concrt-scheduler-policy#2)]  
  
 The [concurrency::PolicyElementKey](../vs140/PolicyElementKey-Enumeration.md) enumeration defines the policy keys that are associated with the Task Scheduler. The following table describes the policy keys and the default value that the runtime uses for each of them.  
  
|Policy Key|Description|Default Value|  
|----------------|-----------------|-------------------|  
|`SchedulerKind`|A [concurrency::SchedulerType](../vs140/SchedulerType-Enumeration.md) value that specifies the type of threads to use to schedule tasks.|`ThreadScheduler` (use normal threads). This is the only valid value for this key.|  
|`MaxConcurrency`|An `unsigned int` value that specifies the maximum number of concurrency resources that the scheduler uses.|[concurrency::MaxExecutionResources](../vs140/MaxExecutionResources-Constant.md)|  
|`MinConcurrency`|An `unsigned int` value that specifies the minimum number of concurrency resources that the scheduler uses.|`1`|  
|`TargetOversubscriptionFactor`|An `unsigned int` value that specifies how many threads to allocate to each processing resource.|`1`|  
|`LocalContextCacheSize`|An `unsigned int` value that specifies the maximum number of contexts that can be cached in the local queue of each virtual processor.|`8`|  
|`ContextStackSize`|An `unsigned int` value that specifies the size of the stack, in kilobytes, to reserve for each context.|`0` (use the default stack size)|  
|`ContextPriority`|An `int` value that specifies the thread priority of each context. This can be any value that you can pass to [SetThreadPriority](http://msdn.microsoft.com/library/windows/desktop/ms686277) or `INHERIT_THREAD_PRIORITY`.|`THREAD_PRIORITY_NORMAL`|  
|`SchedulingProtocol`|A [concurrency::SchedulingProtocolType](../vs140/SchedulingProtocolType-Enumeration.md) value that specifies the scheduling algorithm to use.|`EnhanceScheduleGroupLocality`|  
|`DynamicProgressFeedback`|A [concurrency::DynamicProgressFeedbackType](../vs140/DynamicProgressFeedbackType-Enumeration.md) value that specifies whether to rebalance resources according to statistics-based progress information.<br /><br /> **Note** Do not set this policy to `ProgressFeedbackDisabled` because it is reserved for use by the runtime.|`ProgressFeedbackEnabled`|  
  
 Each scheduler uses its own policy when it schedules tasks. The policies that are associated with one scheduler do not affect the behavior of any other scheduler. In addition, you cannot change the scheduler policy after you create the `Scheduler` object.  
  
> [!IMPORTANT]
>  Use only scheduler policies to control the attributes for threads that the runtime creates. Do not change the thread affinity or priority of threads that are created by the runtime because that might cause undefined behavior.  
  
 The runtime creates a default scheduler for you if you do not explicitly create one. If you want to use the default scheduler in your application, but you want to specify a policy for that scheduler to use, call the [concurrency::Scheduler::SetDefaultSchedulerPolicy](../vs140/Scheduler--SetDefaultSchedulerPolicy-Method.md) method before you schedule parallel work. If you do not call the `Scheduler::SetDefaultSchedulerPolicy` method, the runtime uses the default policy values from the table.  
  
 Use the [concurrency::CurrentScheduler::GetPolicy](../vs140/CurrentScheduler--GetPolicy-Method.md) and the [concurrency::Scheduler::GetPolicy](../vs140/Scheduler--GetPolicy-Method.md) methods to retrieve a copy of the scheduler policy. The policy values that you receive from these methods can differ from the policy values that you specify when you create the scheduler.  
  
## Example  
 To examine examples that use specific scheduler policies to control the behavior of the scheduler, see [How-to: Specify Specific Scheduler Policies](../vs140/How-to--Specify-Specific-Scheduler-Policies.md) and [How-to: Create Agents that Use Specific Scheduler Policies](../vs140/How-to--Create-Agents-that-Use-Specific-Scheduler-Policies.md).  
  
## See Also  
 [Task Scheduler (Concurrency Runtime)](../vs140/Task-Scheduler--Concurrency-Runtime-.md)   
 [How-to: Specify Specific Scheduler Policies](../vs140/How-to--Specify-Specific-Scheduler-Policies.md)   
 [How-to: Create Agents that Use Specific Scheduler Policies](../vs140/How-to--Create-Agents-that-Use-Specific-Scheduler-Policies.md)