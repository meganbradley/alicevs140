---
title: "recursive_timed_mutex Class"
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
ms.assetid: 59cc2d5c-ed80-45f3-a0a8-05652a8ead7e
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# recursive_timed_mutex Class
Represents a *timed mutex type*. Objects of this type are used to enforce mutual exclusion by using time-limited blocking within a program. Unlike objects of type [timed_mutex](../vs140/timed_mutex-Class.md), the effect of calling locking methods for `recursive_timed_mutex` objects is well-defined.  
  
## Syntax  
  
```  
class recursive_timed_mutex;  
```  
  
## Members  
  
### Public Constructors  
  
|Name|Description|  
|----------|-----------------|  
|[recursive_timed_mutex::recursive_timed_mutex Constructor](#recursive_timed_mutex__recursive_timed_mutex_constructor)|Constructs a `recursive_timed_mutex` object that's not locked.|  
|[recursive_timed_mutex::~recursive_timed_mutex Destructor](#recursive_timed_mutex___dtorrecursive_timed_mutex_destructor)|Releases any resources that are used by the `recursive_timed_mutex` object.|  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[recursive_timed_mutex::lock Method](#recursive_timed_mutex__lock_method)|Blocks the calling thread until the thread obtains ownership of the `mutex`.|  
|[recursive_timed_mutex::try_lock Method](#recursive_timed_mutex__try_lock_method)|Attempts to obtain ownership of the `mutex` without blocking.|  
|[recursive_timed_mutex::try_lock_for Method](#recursive_timed_mutex__try_lock_for_method)|Attempts to obtain ownership of the `mutex` for a specified time interval.|  
|[recursive_timed_mutex::try_lock_until Method](#recursive_timed_mutex__try_lock_until_method)|Attempts to obtain ownership of the `mutex` until a specified time.|  
|[recursive_timed_mutex::unlock Method](#recursive_timed_mutex__unlock_method)|Releases ownership of the `mutex`.|  
  
## Requirements  
 **Header:** mutex  
  
 **Namespace:** std  
  
##  <a name="recursive_timed_mutex__lock_method"></a>  recursive_timed_mutex::lock Method  
 Blocks the calling thread until the thread obtains ownership of the `mutex`.  
  
```cpp  
void lock();  
```  
  
### Remarks  
 If the calling thread already owns the `mutex`, the method returns immediately, and the previous lock remains in effect.  
  
##  <a name="recursive_timed_mutex__recursive_timed_mutex_constructor"></a>  recursive_timed_mutex::recursive_timed_mutex Constructor  
 Constructs a `recursive_timed_mutex` object that is not locked.  
  
```cpp  
recursive_timed_mutex();  
```  
  
##  <a name="recursive_timed_mutex___dtorrecursive_timed_mutex_destructor"></a>  recursive_timed_mutex::~recursive_timed_mutex Destructor  
 Releases any resources that are used by the `recursive_timed_mutex` object.  
  
```cpp  
~recursive_timed_mutex();  
```  
  
### Remarks  
 If the object is locked when the destructor runs, the behavior is undefined.  
  
##  <a name="recursive_timed_mutex__try_lock_method"></a>  recursive_timed_mutex::try_lock Method  
 Attempts to obtain ownership of the `mutex` without blocking.  
  
```cpp  
bool try_lock() _NOEXCEPT;  
```  
  
### Return Value  
 `true` if the method successfully obtained ownership of the `mutex` or if the calling thread already owns the `mutex`; otherwise, `false`.  
  
### Remarks  
 If the calling thread already owns the `mutex`, the function immediately returns `true`, and the previous lock remains in effect.  
  
##  <a name="recursive_timed_mutex__try_lock_for_method"></a>  recursive_timed_mutex::try_lock_for Method  
 Attempts to obtain ownership of the `mutex` without blocking.  
  
```cpp  
template<class Rep, class Period>  
   bool try_lock_for(const chrono::duration<Rep, Period>& Rel_time);  
```  
  
### Parameters  
 `Rel_time`  
 A [chrono::duration](../vs140/duration-Class.md) object that specifies the maximum amount of time that the method attempts to obtain ownership of the `mutex`.  
  
### Return Value  
 `true` if the method successfully obtains ownership of the `mutex` or if the calling thread already owns the `mutex`; otherwise, `false`.  
  
### Remarks  
 If the calling thread already owns the `mutex`, the method immediately returns `true`, and the previous lock remains in effect.  
  
##  <a name="recursive_timed_mutex__try_lock_until_method"></a>  recursive_timed_mutex::try_lock_until Method  
 Attempts to obtain ownership of the `mutex` without blocking.  
  
```cpp  
template<class Clock, class Duration>  
   bool try_lock_for(const chrono::time_point<Clock, Duration>& Abs_time);  
bool try_lock_until(const xtime * Abs_time);  
```  
  
### Parameters  
 `Abs_time`  
 A point in time that specifies the threshold after which the method no longer attempts to obtain ownership of the `mutex`.  
  
### Return Value  
 `true` if the method successfully obtains ownership of the `mutex` or if the calling thread already owns the `mutex`; otherwise, `false`.  
  
### Remarks  
 If the calling thread already owns the `mutex`, the method immediately returns `true`, and the previous lock remains in effect.  
  
##  <a name="recursive_timed_mutex__unlock_method"></a>  recursive_timed_mutex::unlock Method  
 Releases ownership of the `mutex`.  
  
```cpp  
void unlock();  
```  
  
### Remarks  
 This method releases ownership of the `mutex` only after it is called as many times as [lock](#recursive_timed_mutex__lock_method), [try_lock](#recursive_timed_mutex__try_lock_method), [try_lock_for](#recursive_timed_mutex__try_lock_for_method), and [try_lock_until](#recursive_timed_mutex__try_lock_until_method) have been called successfully on the `recursive_timed_mutex` object.  
  
 If the calling thread does not own the `mutex`, the behavior is undefined.  
  
## See Also  
 [Header Files](../vs140/C---Standard-Library-Header-Files.md)   
 [<mutex\>](../vs140/-mutex-.md)