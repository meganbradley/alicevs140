---
title: "IUMSScheduler::SetCompletionList Method"
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
ms.assetid: 4c6fa217-b898-4c7b-bec1-6769ade9746a
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IUMSScheduler::SetCompletionList Method
Assigns an `IUMSCompletionList` interface to a UMS thread scheduler.  
  
## Syntax  
  
```  
virtual void SetCompletionList(  
   _Inout_ IUMSCompletionList * pCompletionList  
) =0;  
```  
  
#### Parameters  
 `pCompletionList`  
 The completion list interface for the scheduler. There is a single list per scheduler.  
  
## Remarks  
 The Resource Manager will invoke this method on a scheduler that specifies it wants UMS threads, after the scheduler has requested an initial allocation of resources. The scheduler can use the `IUMSCompletionList` interface to determine when UMS thread proxies have unblocked. It is only valid to access this interface from a thread proxy running on a virtual processor root assigned to the UMS scheduler.  
  
## Requirements  
 **Header:** concrtrm.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [IUMSScheduler Structure](../vs140/IUMSScheduler-Structure.md)   
 [IScheduler Structure](../vs140/IScheduler-Structure.md)   
 [IUMSCompletionList Structure](../vs140/IUMSCompletionList-Structure.md)