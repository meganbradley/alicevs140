---
title: "Context::Unblock Method"
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
ms.assetid: 4bc6323e-d74f-43cc-8f1a-426cf4b4d9a1
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Context::Unblock Method
Unblocks the context and causes it to become runnable.  
  
## Syntax  
  
```  
virtual void Unblock() =0;  
```  
  
## Remarks  
 It is perfectly legal for a call to the `Unblock` method to come before a corresponding call to the [Block](../vs140/Context--Block-Method.md) method. As long as calls to the `Block` and `Unblock` methods are properly paired, the runtime properly handles the natural race of either ordering. An `Unblock` call coming before a `Block` call simply negates the effect of the `Block` call.  
  
 There are several exceptions which can be thrown from this method. If a context attempts to call the `Unblock` method on itself, a [context_self_unblock](../vs140/context_self_unblock-Class.md) exception will be thrown. If calls to `Block` and `Unblock` are not properly paired (for example, two calls to `Unblock` are made for a context which is currently running), a [context_unblock_unbalanced](../vs140/context_unblock_unbalanced-Class.md) exception will be thrown.  
  
 Be aware that there is a critical period between the point where your code publishes its context for another thread to be able to call the `Unblock` method and the point where the actual method call to `Block` is made. During this period, you must not call any method which can in turn block and unblock for its own reasons (for example, acquiring a lock). Calls to the `Block` and `Unblock` method do not track the reason for the blocking and unblocking. Only one object should have ownership of a `Block` and `Unblock` pair.  
  
## Requirements  
 **Header:** concrt.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [Context Class](../vs140/Context-Class.md)   
 [Context::Block Method](../vs140/Context--Block-Method.md)   
 [Task Scheduler (Concurrency Runtime)](../vs140/Task-Scheduler--Concurrency-Runtime-.md)