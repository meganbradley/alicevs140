---
title: "condition_variable_any Class"
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
ms.assetid: d8afe5db-1561-4ec2-8e85-21ea03ee4321
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# condition_variable_any Class
Use the class `condition_variable_any` to wait for an event that has any `mutex` type.  
  
## Syntax  
  
```  
class condition_variable_any;  
```  
  
## Members  
  
### Public Constructors  
  
|Name|Description|  
|----------|-----------------|  
|[condition_variable_any::condition_variable_any Constructor](#condition_variable_any__condition_variable_any_constructor)|Constructs a `condition_variable_any` object.|  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[condition_variable_any::notify_all Method](#condition_variable_any__notify_all_method)|Unblocks all threads that are waiting for the `condition_variable_any` object.|  
|[condition_variable_any::notify_one Method](#condition_variable_any__notify_one_method)|Unblocks one of the threads that are waiting for the `condition_variable_any` object.|  
|[condition_variable_any::wait Method](#condition_variable_any__wait_method)|Blocks a thread.|  
|[condition_variable_any::wait_for Method](#condition_variable_any__wait_for_method)|Blocks a thread, and sets a time interval after which the thread unblocks.|  
|[condition_variable_any::wait_until Method](#condition_variable_any__wait_until_method)|Blocks a thread, and sets a maximum point in time at which the thread unblocks.|  
  
## Requirements  
 **Header:** condition_variable  
  
 **Namespace:** std  
  
##  <a name="condition_variable_any__condition_variable_any_constructor"></a>  condition_variable_any::condition_variable_any Constructor  
 Constructs a `condition_variable_any` object.  
  
```  
condition_variable_any();  
```  
  
### Remarks  
 If not enough memory is available, the constructor throws a [system_error](../vs140/system_error-Class.md) object that has a `not_enough_memory` error code. If the object cannot be constructed because some other resource is not available, the constructor throws a `system_error` object that has a `resource_unavailable_try_again` error code.  
  
##  <a name="condition_variable_any__notify_all_method"></a>  condition_variable_any::notify_all Method  
 Unblocks all threads that are waiting for the `condition_variable_any` object.  
  
```  
void notify_all() _NOEXCEPT;  
```  
  
##  <a name="condition_variable_any__notify_one_method"></a>  condition_variable_any::notify_one Method  
 Unblocks one of the threads that are waiting on the `condition_variable_any` object.  
  
```  
void notify_one() _NOEXCEPT;  
```  
  
##  <a name="condition_variable_any__wait_method"></a>  condition_variable_any::wait Method  
 Blocks a thread.  
  
```  
template <class Lock>  
   void wait(  
      Lock& Lck  
);  
template<class Lock, class Predicate>  
void wait(  
   Lock& Lck,  
   Predicate Pred  
);  
```  
  
### Parameters  
 `Lck`  
 A `mutex` object of any type.  
  
 `Pred`  
 Any expression that returns `true` or `false`.  
  
### Remarks  
 The first method blocks until the `condition_variable_any` object is signaled by a call to [notify_one](../vs140/condition_variable-Class.md#condition_variable__notify_one_method) or [notify_all](../vs140/condition_variable-Class.md#condition_variable__notify_all_method). It can also wake up spuriously.  
  
 The second method in effect executes the following code.  
  
```  
while (!Pred())  
    wait(Lck);  
```  
  
##  <a name="condition_variable_any__wait_for_method"></a>  condition_variable_any::wait_for Method  
 Blocks a thread, and sets a time interval after which the thread unblocks.  
  
```  
template<  
   class Lock,  
   class Rep,  
   class Period  
>  
bool wait_for(  
   Lock& Lck,  
   const chrono::duration< Rep, Period>& Rel_time  
);  
template<  
   class Lock,  
   class Rep,  
   class Period,  
   class Predicate  
>  
bool wait_for(  
   Lock& Lck,  
   const chrono::duration< Rep, Period>& Rel_time, Predicate Pred  
);  
```  
  
### Parameters  
 `Lck`  
 A `mutex` object of any type.  
  
 `Rel_time`  
 A `chrono::duration` object that specifies the amount of time before the thread wakes up.  
  
 `Pred`  
 Any expression that returns `true` or `false`.  
  
### Return Value  
 The first method returns `cv_status::timeout` if the wait terminates when `Rel_time` has elapsed. Otherwise, the method returns `cv_status::no_timeout`.  
  
 The second method returns the value of `Pred`.  
  
### Remarks  
 The first method blocks until the `condition_variable_any` object is signaled by a call to [notify_one](../vs140/condition_variable-Class.md#condition_variable__notify_one_method) or [notify_all](../vs140/condition_variable-Class.md#condition_variable__notify_all_method), or until the time interval `Rel_time` has elapsed. It can also wake up spuriously.  
  
 The second method in effect executes the following code.  
  
```  
while(!Pred())  
   if(wait_for(Lck, Rel_time) == cv_status::timeout)  
      return Pred();  
return true;  
```  
  
##  <a name="condition_variable_any__wait_until_method"></a>  condition_variable_any::wait_until Method  
 Blocks a thread, and sets a maximum point in time at which the thread unblocks.  
  
```  
template<class Lock, class Clock, class Duration>  
   void wait_until(  
      Lock& Lck,   
      const chrono::time_point<Clock, Duration>& Abs_time);  
template<class Lock, class Clock, class Duration, class Predicate>  
   void wait_until(  
      Lock& Lck,  
      const chrono::time_point<Clock, Duration>& Abs_time,  
      Predicate Pred);  
template<class Lock>  
   void wait_until(  
      Lock Lck,  
      const xtime * Abs_time);  
template<class Lock, class Predicate>  
   void wait_until(  
      Lock Lck,  
      const xtime * Abs_time,  
      Predicate Pred);  
```  
  
### Parameters  
 `Lck`  
 A mutex object.  
  
 `Abs_time`  
 A [chrono::time_point](../vs140/time_point-Class.md) object.  
  
 `Pred`  
 Any expression that returns `true` or `false`.  
  
### Return Value  
 Methods that return a `cv_status` type return `cv_status::timeout` if the wait terminates when `Abs_time` elapses. Otherwise, the methods return `cv_status::no_timeout`.  
  
 Methods that return a `bool` return the value of `Pred`.  
  
### Remarks  
 The first method blocks until the `condition_variable` object is signaled by a call to [notify_one](../vs140/condition_variable-Class.md#condition_variable__notify_one_method) or [notify_all](../vs140/condition_variable-Class.md#condition_variable__notify_all_method), or until `Abs_time`. It can also wake up spuriously.  
  
 The second method in effect executes the following code.  
  
```  
while(!Pred())  
   if(wait_until(Lck, Abs_time) == cv_status::timeout)  
      return Pred();  
return true;  
```  
  
 The third and fourth methods use a pointer to an object of type `xtime` to replace the `chrono::time_point` object. The `xtime` object specifies the maximum amount of time to wait for a signal.  
  
## See Also  
 [Header Files](../vs140/C---Standard-Library-Header-Files.md)   
 [<condition_variable>](../vs140/-condition_variable-.md)