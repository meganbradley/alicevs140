---
title: "ISchedulerProxy::CreateOversubscriber Method"
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
ms.assetid: b6d12599-3967-44c1-87e1-b28f3ad463a8
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ISchedulerProxy::CreateOversubscriber Method
Creates a new virtual processor root on the hardware thread associated with an existing execution resource.  
  
## Syntax  
  
```  
virtual IVirtualProcessorRoot * CreateOversubscriber(  
   _Inout_ IExecutionResource * pExecutionResource  
) =0;  
```  
  
#### Parameters  
 `pExecutionResource`  
 An `IExecutionResource` interface that represents the hardware thread you want to oversubscribe.  
  
## Return Value  
 An `IVirtualProcessorRoot` interface.  
  
## Remarks  
 Use this method when your scheduler wants to oversubscribe a particular hardware thread for a limited amount of time. Once you are done with the virtual processor root, you should return it to the resource manager by calling the [Remove](../vs140/IExecutionResource--Remove-Method.md) method on the `IVirtualProcessorRoot` interface.  
  
 You can even oversubscribe an existing virtual processor root, because the `IVirtualProcessorRoot` interface inherits from the `IExecutionResource` interface.  
  
## Requirements  
 **Header:** concrtrm.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [ISchedulerProxy Structure](../vs140/ISchedulerProxy-Structure.md)