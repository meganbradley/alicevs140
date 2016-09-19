---
title: "Context::Block Method"
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
ms.assetid: 9c7a473a-dbea-4d08-961d-114223c4e135
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Context::Block Method
Blocks the current context.  
  
## Syntax  
  
```  
static void __cdecl Block();  
```  
  
## Remarks  
 This method will result in the process' default scheduler being created and/or attached to the calling context if there is no scheduler currently associated with the calling context.  
  
 If the calling context is running on a virtual processor, the virtual processor will find another runnable context to execute or can potentially create a new one.  
  
 After the `Block` method has been called or will be called, you must pair it with a call to the [Unblock](../vs140/Context--Unblock-Method.md) method from another execution context in order for it to run again. Be aware that there is a critical period between the point where your code publishes its context for another thread to be able to call the `Unblock` method and the point where the actual method call to `Block` is made. During this period, you must not call any method which can in turn block and unblock for its own reasons (for example, acquiring a lock). Calls to the `Block` and `Unblock` method do not track the reason for the blocking and unblocking. Only one object should have ownership of a `Block`-`Unblock` pair.  
  
 This method can throw a variety of exceptions, including [scheduler_resource_allocation_error](../vs140/scheduler_resource_allocation_error-Class.md).  
  
## Requirements  
 **Header:** concrt.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [Context Class](../vs140/Context-Class.md)   
 [Context::Unblock Method](../vs140/Context--Unblock-Method.md)   
 [Task Scheduler (Concurrency Runtime)](../vs140/Task-Scheduler--Concurrency-Runtime-.md)