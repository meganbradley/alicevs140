---
title: "ISchedulerProxy::BindContext Method"
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
ms.assetid: 4404bda6-82af-4ed5-80ac-14f3ff3504f7
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ISchedulerProxy::BindContext Method
Associates an execution context with a thread proxy, if it is not already associated with one.  
  
## Syntax  
  
```  
virtual void BindContext(  
   _Inout_ IExecutionContext * pContext  
) =0;  
```  
  
#### Parameters  
 `pContext`  
 An interface to the execution context to associate with a thread proxy.  
  
## Remarks  
 Normally, the [IThreadProxy::SwitchTo](../vs140/IThreadProxy--SwitchTo-Method.md) method will bind a thread proxy to an execution context on demand. There are, however, circumstances where it is necessary to bind a context in advance to ensure that the `SwitchTo` method switches to an already bound context. This is the case on a UMS scheduling context as it cannot call methods that allocate memory, and binding a thread proxy may involve memory allocation if a thread proxy is not readily available in the free pool of the thread proxy factory.  
  
 `invalid_argument` is thrown if the parameter `pContext` has the value `NULL`.  
  
## Requirements  
 **Header:** concrtrm.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [ISchedulerProxy Structure](../vs140/ISchedulerProxy-Structure.md)   
 [ISchedulerProxy::UnbindContext Method](../vs140/ISchedulerProxy--UnbindContext-Method.md)