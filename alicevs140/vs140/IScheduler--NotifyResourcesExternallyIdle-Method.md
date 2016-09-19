---
title: "IScheduler::NotifyResourcesExternallyIdle Method"
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
ms.assetid: f1d79ad1-2d7c-4015-b7a7-7efe7ef23d14
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IScheduler::NotifyResourcesExternallyIdle Method
Notifies this scheduler that the hardware threads represented by the set of virtual processor roots in the array `ppVirtualProcessorRoots` are not being used by other schedulers.  
  
## Syntax  
  
```  
virtual void NotifyResourcesExternallyIdle(  
   _In_reads_(count) IVirtualProcessorRoot ** ppVirtualProcessorRoots,  
   unsigned int count  
) =0;  
```  
  
#### Parameters  
 `ppVirtualProcessorRoots`  
 An array of `IVirtualProcessorRoot` interfaces associated with hardware threads on which other schedulers have become idle.  
  
 `count`  
 The number of `IVirtualProcessorRoot` interfaces in the array.  
  
## Remarks  
 It is possible for a particular hardware thread to be assigned to multiple schedulers at the same time. One reason for this could be that there are not enough hardware threads on the system to satisfy the minimum concurrency for all schedulers, without sharing resources. Another possibility is that resources are temporarily assigned to other schedulers when the owning scheduler is not using them, by way of all its virtual processor roots on that hardware thread being deactivated.  
  
 The subscription level of a hardware thread is denoted by the number of subscribed threads and activated virtual processor roots associated with that hardware thread. From a particular scheduler's point of view, the external subscription level of a hardware thread is the portion of the subscription other schedulers contribute to. Notifications that resources are externally busy are sent to a scheduler when the external subscription level for a hardware thread falls to zero from a previous positive value.  
  
 Notifications via this method are only sent to schedulers that have a policy where the value for the `MinConcurrency` policy key is equal to the value for the `MaxConcurrency` policy key. For more information on scheduler policies, see [SchedulerPolicy](../vs140/SchedulerPolicy-Class.md).  
  
 A scheduler that qualifies for notifications gets a set of initial notifications when it is created, informing it whether the resources it was just assigned are externally busy or idle.  
  
## Requirements  
 **Header:** concrtrm.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [IScheduler Structure](../vs140/IScheduler-Structure.md)   
 [IExecutionResource::CurrentSubscriptionLevel Method](../vs140/IExecutionResource--CurrentSubscriptionLevel-Method.md)   
 [IScheduler::NotifyResourcesExternallyBusy Method](../vs140/IScheduler--NotifyResourcesExternallyBusy-Method.md)