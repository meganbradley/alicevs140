---
title: "promise::set_value Method"
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
ms.assetid: 6d7edbbc-a42c-449a-a881-3b9427e87bb9
caps.latest.revision: 9
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# promise::set_value Method
Atomically stores a value as the result of this `promise` object and sets the *associated asynchronous state* to *ready*.  
  
## Syntax  
  
```  
void promise::set_value(const Ty& Val);  
void promise::set_value(Ty&& Val);  
void promise<Ty&>::set_value(Ty& Val);  
void promise<void>::set_value();  
```  
  
#### Parameters  
 `Val`  
 The value to be stored as the result.  
  
## Remarks  
 If the `promise` object has no associated asynchronous state, this method throws a [future_error](../vs140/future_error-Class.md) that has an error code of `no_state`.  
  
 If [set_exception](../vs140/promise--set_exception-Method.md), [set_exception_at_thread_exit](../vs140/promise--set_exception_at_thread_exit-Method.md), `set_value`, or [set_value_at_thread_exit](../vs140/promise--set_value_at_thread_exit-Method.md) has already been called for a `promise` object that has the same associated asynchronous state, this method throws a `future_error` that has an error code of `promise_already_satisfied`.  
  
 As a result of this method, any threads that are blocked on the associated asynchronous state become unblocked.  
  
 The first method also throws any exception that is thrown when `Val` is copied into the associated asynchronous state. In this situation, the associated asynchronous state is not set to ready.  
  
 The second method also throws any exception that is thrown when `Val` is moved into the associated asynchronous state. In this situation, the associated asynchronous state is not set to ready.  
  
 For the partial specialization `promise<Ty&>`, the stored value is in effect a reference to `Val`.  
  
 For the specialization `promise<void>`, no stored value exists.  
  
## Requirements  
 **Header:** future  
  
 **Namespace:** std  
  
## See Also  
 [promise Class](../vs140/promise-Class.md)   
 [<future\>](../vs140/-future-.md)