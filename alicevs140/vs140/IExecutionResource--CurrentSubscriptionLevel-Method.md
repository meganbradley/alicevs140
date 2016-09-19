---
title: "IExecutionResource::CurrentSubscriptionLevel Method"
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
ms.assetid: 50059f0d-3ec6-4915-8cbe-13444ecbc33e
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IExecutionResource::CurrentSubscriptionLevel Method
Returns the number of activated virtual processor roots and subscribed external threads currently associated with the underlying hardware thread this execution resource represents.  
  
## Syntax  
  
```  
virtual unsigned int CurrentSubscriptionLevel() const =0;  
```  
  
## Return Value  
 The current subscription level.  
  
## Remarks  
 The subscription level tells you how many running threads are associated with the hardware thread. This only includes threads the Resource Manager is aware of in the form of subscribed threads, and virtual processor roots that are actively executing thread proxies.  
  
 Calling the method [ISchedulerProxy::SubscribeCurrentThread](../vs140/ISchedulerProxy--SubscribeCurrentThread-Method.md), or the method [ISchedulerProxy::RequestInitialVirtualProcessors](../vs140/ISchedulerProxy--RequestInitialVirtualProcessors-Method.md) with the parameter `doSubscribeCurrentThread` set to the value `true` increments the subscription level of a hardware thread by one. They also return an `IExecutionResource` interface representing the subscription. A corresponding call to the [IExecutionResource::Remove](../vs140/IExecutionResource--Remove-Method.md) decrements the hardware thread's subscription level by one.  
  
 The act of activating a virtual processor root using the method [IVirtualProcessorRoot::Activate](../vs140/IVirtualProcessorRoot--Activate-Method.md) increments the subscription level of a hardware thread by one. The methods [IVirtualProcessorRoot::Deactivate](../vs140/IVirtualProcessorRoot--Deactivate-Method.md), or [IExecutionResource::Remove](../vs140/IExecutionResource--Remove-Method.md) decrement the subscription level by one when invoked on an activated virtual processor root.  
  
 The Resource Manager uses subscription level information as one of the ways in which to determine when to move resources between schedulers.  
  
## Requirements  
 **Header:** concrtrm.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [IExecutionResource Structure](../vs140/IExecutionResource-Structure.md)