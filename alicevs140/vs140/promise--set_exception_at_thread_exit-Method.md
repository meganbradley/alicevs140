---
title: "promise::set_exception_at_thread_exit Method"
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
ms.assetid: 0cdc2f20-fa0d-4ec4-b61e-5a98badde3fc
caps.latest.revision: 9
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# promise::set_exception_at_thread_exit Method
Atomically sets the result of this `promise` to indicate an exception, delivering the notification only after all thread-local objects in the current thread have been destroyed (usually at thread exit).  
  
## Syntax  
  
```  
void set_exception_at_thread_exit(exception_ptr Exc);  
```  
  
#### Parameters  
 `Exc`  
 An [exception_ptr](../vs140/Transporting-Exceptions-Between-Threads.md) that's stored by this method as the exception result.  
  
## Remarks  
 If the promise object has no *associated asynchronous state*, this method throws a [future_error](../vs140/future_error-Class.md) that has an error code of `no_state`.  
  
 If [set_exception](../vs140/promise--set_exception-Method.md), `set_exception_at_thread_exit`, [set_value](../vs140/promise--set_value-Method.md), or [set_value_at_thread_exit](../vs140/promise--set_value_at_thread_exit-Method.md) has already been called for a `promise` object that has the same associated asynchronous state, this method throws a `future_error` that has an error code of `promise_already_satisfied`.  
  
 In contrast to [set_exception](../vs140/promise--set_exception-Method.md), this method does not set the associated asynchronous state to ready until after all thread-local objects in the current thread have been destroyed. Typically, threads that are blocked on the associated asynchronous state are not unblocked until the current thread exits.  
  
## Requirements  
 **Header:** future  
  
 **Namespace:** std  
  
## See Also  
 [promise Class](../vs140/promise-Class.md)   
 [<future\>](../vs140/-future-.md)