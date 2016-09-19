---
title: "ISchedulerProxy::Shutdown Method"
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
ms.assetid: 95eb2a24-8ff2-4d4a-b150-101b9110af01
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ISchedulerProxy::Shutdown Method
Notifies the Resource Manager that the scheduler is shutting down. This will cause the Resource Manager to immediately reclaim all resources granted to the scheduler.  
  
## Syntax  
  
```  
virtual void Shutdown() =0;  
```  
  
## Remarks  
 All `IExecutionContext` interfaces the scheduler received as a result of subscribing an external thread using the methods `ISchedulerProxy::RequestInitialVirtualProcessors` or `ISchedulerProxy::SubscribeCurrentThread` must be returned to the Resource Manager using `IExecutionResource::Remove` before a scheduler shuts itself down.  
  
 If your scheduler had any deactivated virtual processor roots, you must activate them using [IVirtualProcessorRoot::Activate](../vs140/IVirtualProcessorRoot--Activate-Method.md), and have the thread proxies executing on them leave the `Dispatch` method of the execution contexts they are dispatching before you invoke `Shutdown` on a scheduler proxy.  
  
 It is not necessary for the scheduler to individually return all of the virtual processor roots the Resource Manager granted to it via calls to the `Remove` method because all virtual processors roots will be returned to the Resource Manager at shutdown.  
  
## Requirements  
 **Header:** concrtrm.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [ISchedulerProxy Structure](../vs140/ISchedulerProxy-Structure.md)   
 [ISchedulerProxy::RequestInitialVirtualProcessors Method](../vs140/ISchedulerProxy--RequestInitialVirtualProcessors-Method.md)   
 [ISchedulerProxy::SubscribeCurrentThread Method](../vs140/ISchedulerProxy--SubscribeCurrentThread-Method.md)   
 [IExecutionResource::Remove Method](../vs140/IExecutionResource--Remove-Method.md)