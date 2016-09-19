---
title: "IResourceManager::RegisterScheduler Method"
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
ms.assetid: c7010591-4513-4cb9-96cf-606ac1af77a3
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IResourceManager::RegisterScheduler Method
Registers a scheduler with the Resource Manager. Once the scheduler is registered, it should communicate with the Resource Manager using the `ISchedulerProxy` interface that is returned.  
  
## Syntax  
  
```  
virtual ISchedulerProxy *RegisterScheduler(  
   _Inout_ IScheduler * pScheduler,  
   unsigned int version  
) =0;  
```  
  
#### Parameters  
 `pScheduler`  
 An `IScheduler` interface to the scheduler to be registered.  
  
 `version`  
 The version of communication interface the scheduler is using to communicate with the Resource Manager. Using a version allows the Resource Manager to evolve the communication interface while allowing schedulers to obtain access to older features. Schedulers that wish to use Resource Manager features present in Visual Studio 2010 should use the version `CONCRT_RM_VERSION_1`.  
  
## Return Value  
 The `ISchedulerProxy` interface the Resource Manager has associated with your scheduler. Your scheduler should use this interface to communicate with Resource Manager from this point on.  
  
## Remarks  
 Use this method to initiate communication with the Resource Manager. The method associates the `IScheduler` interface for your scheduler with an `ISchedulerProxy` interface and hands it back to you. You can use the returned interface to request execution resources for use by your scheduler, or to subscribe threads with the Resource Manager. The Resource Manager will use policy elements from the scheduler policy returned by the [IScheduler::GetPolicy](../vs140/IScheduler--GetPolicy-Method.md) method to determine what type of threads the scheduler will need to execute work. If your `SchedulerKind` policy key has the value `UmsThreadDefault` and the value is read back out of the policy as the value `UmsThreadDefault`, the `IScheduler` interface passed to the method must be an `IUMSScheduler` interface.  
  
 The method throws an `invalid_argument` exception if the parameter `pScheduler` has the value `NULL` or if the parameter `version` is not a valid version for the communication interface.  
  
## Requirements  
 **Header:** concrtrm.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [IResourceManager Structure](../vs140/IResourceManager-Structure.md)   
 [IScheduler Structure](../vs140/IScheduler-Structure.md)   
 [ISchedulerProxy Structure](../vs140/ISchedulerProxy-Structure.md)   
 [SchedulerPolicy Class](../vs140/SchedulerPolicy-Class.md)   
 [PolicyElementKey Enumeration](../vs140/PolicyElementKey-Enumeration.md)