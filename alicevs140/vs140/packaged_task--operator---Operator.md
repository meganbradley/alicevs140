---
title: "packaged_task::operator() Operator"
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
ms.assetid: b880b3ed-836c-4191-9b5f-9a49529f91e3
caps.latest.revision: 7
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# packaged_task::operator() Operator
Calls the callable object that's stored in the *associated asynchronous state*, atomically stores the returned value, and sets the state to *ready*.  
  
## Syntax  
  
```cpp  
void operator()(ArgTypes... args);  
```  
  
## Remarks  
 If the `packaged_task` object doesn't have an associated asynchronous state, this method throws a [future_error](../vs140/future_error-Class.md) that has an error code of `no_state`.  
  
 If this method or [make_ready_at_thread_exit](../vs140/packaged_task--make_ready_at_thread_exit-Method.md) has already been called for a `packaged_task` object that has the same associated asynchronous state, the method throws a `future_error` that has an error code of `promise_already_satisfied`.  
  
 Otherwise, this operator calls `INVOKE(fn, args..., Ty)`, where *fn* is the callable object that's stored in the associated asynchronous state. Any returned value is stored atomically as the returned result of the associated asynchronous state, and the state is set to ready. As a result, any threads that are blocked on the associated asynchronous state become unblocked.  
  
## Requirements  
 **Header:** future  
  
 **Namespace:** std  
  
## See Also  
 [packaged_task Class](../vs140/packaged_task-Class.md)   
 [<future\>](../vs140/-future-.md)