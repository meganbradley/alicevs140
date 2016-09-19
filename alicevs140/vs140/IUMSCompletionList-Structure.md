---
title: "IUMSCompletionList Structure"
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
ms.assetid: 81b5250e-3065-492c-b20d-2cdabf12271a
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IUMSCompletionList Structure
Represents a UMS completion list. When a UMS thread blocks, the scheduler's designated scheduling context is dispatched in order to make a decision of what to schedule on the underlying virtual processor root while the original thread is blocked. When the original thread unblocks, the operating system queues it to the completion list which is accessible through this interface. The scheduler can query the completion list on the designated scheduling context or any other place it searches for work.  
  
## Syntax  
  
```  
struct IUMSCompletionList;  
```  
  
## Members  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[IUMSCompletionList::GetUnblockNotifications Method](#iumscompletionlist__getunblocknotifications_method)|Retrieves a chain of                                         `IUMSUnblockNotification` interfaces representing execution contexts whose associated thread proxies have unblocked since the last time this method was invoked.|  
  
## Remarks  
 A scheduler must be extraordinarily careful about what actions are performed after utilizing this interface to dequeue items from the completion list. The items should be placed on the scheduler's list of runnable contexts and be generally accessible as soon as possible. It is entirely possible that one of the dequeued items has been given ownership of an arbitrary lock. The scheduler can make no arbitrary function calls that may block between the call to dequeue items and the placement of those items on a list that can be generally accessed from within the scheduler.  
  
## Inheritance Hierarchy  
 `IUMSCompletionList`  
  
## Requirements  
 **Header:** concrtrm.h  
  
 **Namespace:** concurrency  
  
##  <a name="iumscompletionlist__getunblocknotifications_method"></a>  IUMSCompletionList::GetUnblockNotifications Method  
 Retrieves a chain of                 `IUMSUnblockNotification` interfaces representing execution contexts whose associated thread proxies have unblocked since the last time this method was invoked.  
  
```  
virtual IUMSUnblockNotification *GetUnblockNotifications() =0;  
```  
  
### Return Value  
 A chain of                         `IUMSUnblockNotification` interfaces.  
  
### Remarks  
 The returned notifications are invalid once the execution contexts are rescheduled.  
  
## See Also  
 [concurrency Namespace](../vs140/concurrency-Namespace.md)   
 [IUMSScheduler Structure](../vs140/IUMSScheduler-Structure.md)   
 [IUMSUnblockNotification Structure](../vs140/IUMSUnblockNotification-Structure.md)