---
title: "promise Class"
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
ms.assetid: 2931558c-d94a-4ba1-ac4f-20bf7b6e23f9
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# promise Class
Describes an *asynchronous provider*.  
  
## Syntax  
  
```  
template<class Ty>  
class promise;  
```  
  
## Members  
  
### Public Constructors  
  
|Name|Description|  
|----------|-----------------|  
|[promise::promise Constructor](#promise__promise_constructor)|Constructs a `promise` object.|  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[promise::get_future Method](#promise__get_future_method)|Returns a [future](../vs140/future-Class.md) associated with this promise.|  
|[promise::set_exception Method](#promise__set_exception_method)|Atomically sets the result of this promise to indicate an exception.|  
|[promise::set_exception_at_thread_exit Method](#promise__set_exception_at_thread_exit_method)|Atomically sets the result of this promise to indicate an exception, and delivers the notification only after all thread-local objects in the current thread have been destroyed (usually at thread exit).|  
|[promise::set_value Method](#promise__set_value_method)|Atomically sets the result of this promise to indicate a value.|  
|[promise::set_value_at_thread_exit Method](#promise__set_value_at_thread_exit_method)|Atomically sets the result of this promise to indicate a value, and delivers the notification only after all thread-local objects in the current thread have been destroyed (usually at thread exit).|  
|[promise::swap Method](#promise__swap_method)|Exchanges the *associated asynchronous state* of this promise with that of a specified promise object.|  
  
### Public Operators  
  
|Name|Description|  
|----------|-----------------|  
|[promise::operator= Operator](#promise__operator_eq)|Assignment of the shared state of this promise object.|  
  
## Inheritance Hierarchy  
 `promise`  
  
## Requirements  
 **Header:** future  
  
 **Namespace:** std  
  
##  <a name="promise__get_future_method"></a>  promise::get_future Method  
 Returns a [future](../vs140/future-Class.md) object that has the same *associated asynchronous state* as this promise.  
  
```  
future<Ty> get_future();  
```  
  
### Remarks  
 If the promise object is empty, this method throws a [future_error](../vs140/future_error-Class.md) that has an [error_code](../vs140/error_code-Class.md) of `no_state`.  
  
 If this method has already been called for a promise object that has the same associated asynchronous state, the method throws a `future_error` that has an `error_code` of `future_already_retrieved`.  
  
##  <a name="promise__operator_eq"></a>  promise::operator=  
 Transfers the *associated asynchronous state* from a specified `promise` object.  
  
```  
promise& operator=(  
   promise&& Other  
) _NOEXCEPT;  
```  
  
### Parameters  
 `Other`  
 A `promise` object.  
  
### Return Value  
 `*this`  
  
### Remarks  
 This operator transfers the associated asynchronous state from `Other`. After the transfer, `Other` is *empty*.  
  
##  <a name="promise__promise_constructor"></a>  promise::promise Constructor  
 Constructs a `promise` object.  
  
```  
promise();  
template<class Alloc>  
promise(  
   allocator_arg_t,  
   const Alloc& Al  
);  
promise(  
   promise&& Other  
) _NOEXCEPT;  
```  
  
### Parameters  
 `Al`  
 A memory allocator. See [<allocators\>](../vs140/-allocators-.md) for more information.  
  
 `Other`  
 A `promise` object.  
  
### Remarks  
 The first constructor constructs an *empty*`promise` object.  
  
 The second constructor constructs an empty `promise` object and uses `Al` for memory allocation.  
  
 The third constructor constructs a `promise` object and transfers the associated asynchronous state from `Other`, and leaves `Other` empty.  
  
##  <a name="promise__set_exception_method"></a>  promise::set_exception Method  
 Atomically stores an exception as the result of this `promise` object and sets the *associated asynchronous state* to *ready*.  
  
```  
void set_exception(exception_ptr Exc);  
```  
  
### Parameters  
 `Exc`  
 An [exception_ptr](../vs140/Transporting-Exceptions-Between-Threads.md) that's stored by this method as the exception result.  
  
### Remarks  
 If the `promise` object has no associated asynchronous state, this method throws a [future_error](../vs140/future_error-Class.md) that has an error code of `no_state`.  
  
 If `set_exception`, [set_exception_at_thread_exit](#promise__set_exception_at_thread_exit_method), [set_value](#promise__set_value_method), or [set_value_at_thread_exit](#promise__set_value_at_thread_exit_method) has already been called for a `promise` object that has the same associated asynchronous state, this method throws a `future_error` that has an error code of `promise_already_satisfied`.  
  
 As a result of this method, any threads that are blocked on the associated asynchronous state become unblocked.  
  
##  <a name="promise__set_exception_at_thread_exit_method"></a>  promise::set_exception_at_thread_exit Method  
 Atomically sets the result of this `promise` to indicate an exception, delivering the notification only after all thread-local objects in the current thread have been destroyed (usually at thread exit).  
  
```  
void set_exception_at_thread_exit(exception_ptr Exc);  
```  
  
### Parameters  
 `Exc`  
 An [exception_ptr](../vs140/Transporting-Exceptions-Between-Threads.md) that's stored by this method as the exception result.  
  
### Remarks  
 If the promise object has no *associated asynchronous state*, this method throws a [future_error](../vs140/future_error-Class.md) that has an error code of `no_state`.  
  
 If [set_exception](#promise__set_exception_method), `set_exception_at_thread_exit`, [set_value](#promise__set_value_method), or [set_value_at_thread_exit](#promise__set_value_at_thread_exit_method) has already been called for a `promise` object that has the same associated asynchronous state, this method throws a `future_error` that has an error code of `promise_already_satisfied`.  
  
 In contrast to [set_exception](#promise__set_exception_method), this method does not set the associated asynchronous state to ready until after all thread-local objects in the current thread have been destroyed. Typically, threads that are blocked on the associated asynchronous state are not unblocked until the current thread exits.  
  
##  <a name="promise__set_value_method"></a>  promise::set_value Method  
 Atomically stores a value as the result of this `promise` object and sets the *associated asynchronous state* to *ready*.  
  
```  
void promise::set_value(const Ty& Val);  
void promise::set_value(Ty&& Val);  
void promise<Ty&>::set_value(Ty& Val);  
void promise<void>::set_value();  
```  
  
### Parameters  
 `Val`  
 The value to be stored as the result.  
  
### Remarks  
 If the `promise` object has no associated asynchronous state, this method throws a [future_error](../vs140/future_error-Class.md) that has an error code of `no_state`.  
  
 If [set_exception](#promise__set_exception_method), [set_exception_at_thread_exit](#promise__set_exception_at_thread_exit_method), `set_value`, or [set_value_at_thread_exit](#promise__set_value_at_thread_exit_method) has already been called for a `promise` object that has the same associated asynchronous state, this method throws a `future_error` that has an error code of `promise_already_satisfied`.  
  
 As a result of this method, any threads that are blocked on the associated asynchronous state become unblocked.  
  
 The first method also throws any exception that is thrown when `Val` is copied into the associated asynchronous state. In this situation, the associated asynchronous state is not set to ready.  
  
 The second method also throws any exception that is thrown when `Val` is moved into the associated asynchronous state. In this situation, the associated asynchronous state is not set to ready.  
  
 For the partial specialization `promise<Ty&>`, the stored value is in effect a reference to `Val`.  
  
 For the specialization `promise<void>`, no stored value exists.  
  
##  <a name="promise__set_value_at_thread_exit_method"></a>  promise::set_value_at_thread_exit Method  
 Atomically stores a value as the result of this `promise` object.  
  
```  
void promise::set_value_at_thread_exit(const Ty& Val);  
void promise::set_value_at_thread_exit(Ty&& Val);  
void promise<Ty&>::set_value_at_thread_exit(Ty& Val);  
void promise<void>::set_value_at_thread_exit();  
```  
  
### Parameters  
 `Val`  
 The value to be stored as the result.  
  
### Remarks  
 If the promise object has no *associated asynchronous state*, this method throws a [future_error](../vs140/future_error-Class.md) that has an error code of `no_state`.  
  
 If [set_exception](#promise__set_exception_method), [set_exception_at_thread_exit](#promise__set_exception_at_thread_exit_method), [set_value](#promise__set_value_method), or `set_value_at_thread_exit` has already been called for a `promise` object that has the same associated asynchronous state, this method throws a `future_error` that has an error code of `promise_already_satisfied`.  
  
 In contrast to `set_value`, the associated asynchronous state is not set to ready until after all thread-local objects in the current thread have been destroyed. Typically, threads that are blocked on the associated asynchronous state are not unblocked until the current thread exits.  
  
 The first method also throws any exception that is thrown when `Val` is copied into the associated asynchronous state.  
  
 The second method also throws any exception that is thrown when `Val` is moved into the associated asynchronous state.  
  
 For the partial specialization `promise<Ty&>`, the stored value is effectively a reference to `Val`.  
  
 For the specialization `promise<void>`, no stored value exists.  
  
##  <a name="promise__swap_method"></a>  promise::swap Method  
 Exchanges the *associated asynchronous state* of this promise object with that of a specified object.  
  
```  
void swap(promise& Other) _NOEXCEPT;  
```  
  
### Parameters  
 `Other`  
 A `promise` object.  
  
## See Also  
 [Header Files](../vs140/C---Standard-Library-Header-Files.md)