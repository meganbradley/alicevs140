---
title: "IExecutionResource::Remove Method"
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
ms.assetid: 0ca7b334-a865-40aa-9ab2-ac9485597168
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IExecutionResource::Remove Method
Returns this execution resource to the Resource Manager.  
  
## Syntax  
  
```  
virtual void Remove(  
   _Inout_ IScheduler * pScheduler  
) =0;  
```  
  
#### Parameters  
 `pScheduler`  
 An interface to the scheduler making the request to remove this execution resource.  
  
## Remarks  
 Use this method to return standalone execution resources as well as execution resources associated with virtual processor roots to the Resource Manager.  
  
 If this is a standalone execution resource you received from either of the methods [ISchedulerProxy::SubscribeCurrentThread](../vs140/ISchedulerProxy--SubscribeCurrentThread-Method.md) or [ISchedulerProxy::RequestInitialVirtualProcessors](../vs140/ISchedulerProxy--RequestInitialVirtualProcessors-Method.md), calling the method `Remove` will end the thread subscription that the resource was created to represent. You are required to end all thread subscriptions before shutting down a scheduler proxy, and must call `Remove` from the thread that created the subscription.  
  
 Virtual processor roots, too, can be returned to the Resource Manager by invoking the `Remove` method, because the interface `IVirtualProcessorRoot` inherits from the `IExecutionResource` interface. You may need to return a virtual processor root either in response to a call to the [IScheduler::RemoveVirtualProcessors](../vs140/IScheduler--RemoveVirtualProcessors-Method.md) method, or when you are done with an oversubscribed virtual processor root you obtained from the [ISchedulerProxy::CreateOversubscriber](../vs140/ISchedulerProxy--CreateOversubscriber-Method.md) method. For virtual processor roots, there are no restrictions on which thread can invoke the `Remove` method.  
  
 `invalid_argument` is thrown if the parameter `pScheduler` is set to `NULL`.  
  
 `invalid_operation` is thrown if the parameter `pScheduler` is different from the scheduler that this execution resource was created for, or, with a standalone execution resource, if the current thread is different from the thread that created the thread subscription.  
  
## Requirements  
 **Header:** concrtrm.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [IExecutionResource Structure](../vs140/IExecutionResource-Structure.md)   
 [invalid_argument Class](../vs140/invalid_argument-Class.md)   
 [invalid_operation Class](../vs140/invalid_operation-Class.md)