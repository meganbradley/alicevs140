---
title: "condition_variable Class"
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
ms.assetid: 80b1295c-b73d-4d46-b664-6e183f2eec1b
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# condition_variable Class
Use the `condition_variable` class to wait for an event when you have a `mutex` of type `unique_lock<mutex>`. Objects of this type may have better performance than objects of type [condition_variable_any<unique_lock<mutex\>>](../vs140/condition_variable_any-Class.md).  
  
## Syntax  
  
```  
class condition_variable;  
```  
  
## Members  
  
### Public Constructors  
  
|Name|Description|  
|----------|-----------------|  
|[condition_variable::condition_variable Constructor](#condition_variable__condition_variable_constructor)|Constructs a `condition_variable` object.|  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[condition_variable::native_handle Method](#condition_variable__native_handle_method)|Returns the implementation-specific type representing the condition_variable handle.|  
|[condition_variable::notify_all Method](#condition_variable__notify_all_method)|Unblocks all threads that are waiting for the `condition_variable` object.|  
|[condition_variable::notify_one Method](#condition_variable__notify_one_method)|Unblocks one of the threads that are waiting for the `condition_variable` object.|  
|[condition_variable::wait Method](#condition_variable__wait_method)|Blocks a thread.|  
|[condition_variable::wait_for Method](#condition_variable__wait_for_method)|Blocks a thread, and sets a time interval after which the thread unblocks.|  
|[condition_variable::wait_until Method](#condition_variable__wait_until_method)|Blocks a thread, and sets a maximum point in time at which the thread unblocks.|  
  
## Requirements  
 **Header:** condition_variable  
  
 **Namespace:** std  
  
##  <a name="condition_variable__condition_variable_constructor"></a>  condition_variable::condition_variable Constructor  
 Constructs a `condition_variable` object.  
  
```  
condition_variable();  
```  
  
### Remarks  
 If not enough memory is available, the constructor throws a [system_error](../vs140/system_error-Class.md) object that has a `not_enough_memory` error code. If the object cannot be constructed because some other resource is not available, the constructor throws a `system_error` object that has a `resource_unavailable_try_again` error code.  
  
##  <a name="condition_variable__native_handle_method"></a>  condition_variable::native_handle Method  
 Returns the implementation-specific type that represents the condition_variable handle.  
  
```  
native_handle_type native_handle();  
```  
  
### Return Value  
 `native_handle_type` is defined as a pointer to Concurrency Runtime internal data structures.  
  
##  <a name="condition_variable__notify_all_method"></a>  condition_variable::notify_all Method  
 Unblocks all threads that are waiting for the `condition_variable` object.  
  
```  
void notify_all() _NOEXCEPT;  
```  
  
##  <a name="condition_variable__notify_one_method"></a>  condition_variable::notify_one Method  
 Unblocks one of the threads that are waiting on the `condition_variable` object.  
  
```  
void notify_one() _NOEXCEPT;  
```  
  
##  <a name="condition_variable__wait_method"></a>  condition_variable::wait Method  
 Blocks a thread.  
  
```  
void wait(  
   unique_lock<mutex>& Lck  
);  
template<class Predicate>  
void wait(  
   unique_lock<mutex>& Lck,  
   Predicate Pred  
);  
```  
  
### Parameters  
 `Lck`  
 A [unique_lock<mutex\>](../vs140/unique_lock-Class.md) object.  
  
 `Pred`  
 Any expression that returns `true` or `false`.  
  
### Remarks  
 The first method blocks until the `condition_variable` object is signaled by a call to [notify_one](#condition_variable__notify_one_method) or [notify_all](#condition_variable__notify_all_method). It can also wake up spuriously.  
  
 In effect, the second method executes the following code.  
  
```cpp  
while(!Pred())  
    wait(Lck);  
```  
  
##  <a name="condition_variable__wait_for_method"></a>  condition_variable::wait_for Method  
 Blocks a thread, and sets a time interval after which the thread unblocks.  
  
```  
template<  
   class Rep,  
   class Period  
>  
cv_status wait_for(  
   unique_lock<mutex>& Lck,  
   const chrono::duration< Rep, Period>& Rel_time  
);  
template<  
   class Rep,  
   class Period,  
   class Predicate  
>  
bool wait_for(  
   unique_lock<mutex>& Lck,  
   const chrono::duration< Rep, Period>& Rel_time, Predicate Pred  
);  
```  
  
### Parameters  
 `Lck`  
 A [unique_lock<mutex\>](../vs140/unique_lock-Class.md) object.  
  
 `Rel_time`  
 A `chrono::duration` object that specifies the amount of time before the thread wakes up.  
  
 `Pred`  
 Any expression that returns `true` or `false`.  
  
### Return Value  
 The first method returns `cv_status::timeout` if the wait terminates when `Rel_time` has elapsed. Otherwise, the method returns `cv_status::no_timeout`.  
  
 The second method returns the value of `Pred`.  
  
### Remarks  
 The first method blocks until the `condition_variable` object is signaled by a call to [notify_one](#condition_variable__notify_one_method) or [notify_all](#condition_variable__notify_all_method) or until the time interval `Rel_time` has elapsed. It can also wake up spuriously.  
  
 In effect, the second method executes the following code.  
  
```css  
while(!Pred())  
   if(wait_for(Lck, Rel_time) == cv_status::timeout)  
      return Pred();  
return true;  
```  
  
##  <a name="condition_variable__wait_until_method"></a>  condition_variable::wait_until Method  
 Blocks a thread, and sets a maximum point in time at which the thread unblocks.  
  
```  
template<  
   class Clock,  
   class Duration  
>  
cv_status wait_until(  
   unique_lock<mutex>& Lck,  
   const chrono::time_point< Clock, Duration>& Abs_time  
);  
template<  
   class Clock,  
   class Duration,  
   class Predicate  
>  
bool wait_until(  
   unique_lock<mutex>& Lck,  
   const chrono::time_point< Clock, Duration>& Abs_time, Predicate Pred  
);  
cv_status wait_until(  
   unique_lock<mutex>& Lck,  
   const xtime * Abs_time  
);  
template<class Predicate>  
bool wait_until(  
   unique_lock<mutex>& Lck,  
   const xtime * Abs_time, Predicate Pred  
);  
```  
  
### Parameters  
 `Lck`  
 A [unique_lock<mutex\>](../vs140/unique_lock-Class.md) object.  
  
 `Abs_time`  
 A [chrono::time_point](../vs140/time_point-Class.md) object.  
  
 `Pred`  
 Any expression that returns `true` or `false`.  
  
### Return Value  
 Methods that return a `cv_status` type return `cv_status::timeout` if the wait terminates when `Abs_time` elapses. Otherwise, the methods return `cv_status::no_timeout`.  
  
 Methods that return a `bool` return the value of `Pred`.  
  
### Remarks  
 The first method blocks until the `condition_variable` object is signaled by a call to [notify_one](#condition_variable__notify_one_method) or [notify_all](#condition_variable__notify_all_method) or until `Abs_time`. It can also wake up spuriously.  
  
 In effect, the second method executes the following code  
  
```cpp  
while(!Pred())  
   if(wait_until(Lck, Abs_time) == cv_status::timeout)  
      return Pred();  
return true;  
```  
  
 The third and fourth methods use a pointer to an object of type `xtime` to replace the `chrono::time_point` object. The `xtime` object specifies the maximum amount of time to wait for a signal.  
  
## See Also  
 [Header Files](../vs140/C---Standard-Library-Header-Files.md)   
 [<condition_variable>](../vs140/-condition_variable-.md)