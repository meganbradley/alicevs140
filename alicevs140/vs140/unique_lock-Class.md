---
title: "unique_lock Class"
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
ms.assetid: f4ed8ba9-c8af-446f-8ef0-0b356bad14bd
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# unique_lock Class
Represents a template that can be instantiated to create objects that manage the locking and unlocking of a `mutex`.  
  
## Syntax  
  
```  
template<class Mutex>  
class unique_lock;  
```  
  
## Remarks  
 The template argument `Mutex` must name a *mutex type*.  
  
 Internally, a `unique_lock` stores a pointer to an associated `mutex` object and a `bool` that indicates whether the current thread owns the `mutex`.  
  
## Members  
  
### Public Typedefs  
  
|Name|Description|  
|----------|-----------------|  
|`unique_lock::mutex_type`|Synonym for the template argument `Mutex`.|  
  
### Public Constructors  
  
|Name|Description|  
|----------|-----------------|  
|[unique_lock::unique_lock Constructor](#unique_lock__unique_lock_constructor)|Constructs a `unique_lock` object.|  
|[unique_lock::~unique_lock Destructor](#unique_lock___dtorunique_lock_destructor)|Releases any resources that are associated with the `unique_lock` object.|  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[unique_lock::lock Method](#unique_lock__lock_method)|Blocks the calling thread until the thread obtains ownership of the associated `mutex`.|  
|[unique_lock::mutex Method](#unique_lock__mutex_method)|Retrieves the stored pointer to the associated `mutex`.|  
|[unique_lock::owns_lock Method](#unique_lock__owns_lock_method)|Specifies whether the calling thread owns the associated `mutex`.|  
|[unique_lock::release Method](#unique_lock__release_method)|Disassociates the `unique_lock` object from the associated `mutex` object.|  
|[unique_lock::swap Method](#unique_lock__swap_method)|Swaps the associated `mutex` and ownership status with that of a specified object.|  
|[unique_lock::try_lock Method](#unique_lock__try_lock_method)|Attempts to obtain ownership of the associated `mutex` without blocking.|  
|[unique_lock::try_lock_for Method](#unique_lock__try_lock_for_method)|Attempts to obtain ownership of the associated `mutex` without blocking.|  
|[unique_lock::try_lock_until Method](#unique_lock__try_lock_until_method)|Attempts to obtain ownership of the associated `mutex` without blocking.|  
|[unique_lock::unlock Method](#unique_lock__unlock_method)|Releases ownership of the associated `mutex`.|  
  
### Public Operators  
  
|Name|Description|  
|----------|-----------------|  
|[unique_lock::operator bool Operator](#unique_lock__operator_bool)|Specifies whether the calling thread has ownership of the associated `mutex`.|  
|[unique_lock::operator= Operator](#unique_lock__operator_eq)|Copies the stored `mutex` pointer and associated ownership status from a specified object.|  
  
## Inheritance Hierarchy  
 `unique_lock`  
  
## Requirements  
 **Header:** mutex  
  
 **Namespace:** std  
  
##  <a name="unique_lock__lock_method"></a>  unique_lock::lock Method  
 Blocks the calling thread until the thread obtains ownership of the associated `mutex`.  
  
```cpp  
void lock();  
```  
  
### Remarks  
 If the stored `mutex` pointer is `null`, this method throws a [system_error](../vs140/system_error-Class.md) that has an error code of `operation_not_permitted`.  
  
 If the calling thread already owns the associated `mutex`, this method throws a `system_error` that has an error code of `resource_deadlock_would_occur`.  
  
 Otherwise, this method calls `lock` on the associated `mutex` and sets the internal thread ownership flag to `true`.  
  
##  <a name="unique_lock__mutex_method"></a>  unique_lock::mutex Method  
 Retrieves the stored pointer to the associated `mutex`.  
  
```cpp  
mutex_type *mutex() const _NOEXCEPT;  
```  
  
##  <a name="unique_lock__operator_bool"></a>  unique_lock::operator bool  
 Specifies whether the calling thread has ownership of the associated mutex.  
  
```cpp  
explicit operator bool() _NOEXCEPT  
```  
  
### Return Value  
 `true` if the thread owns the mutex; otherwise `false`.  
  
##  <a name="unique_lock__operator_eq"></a>  unique_lock::operator=  
 Copies the stored `mutex` pointer and associated ownership status from a specified object.  
  
```cpp  
unique_lock& operator=(  
   unique_lock&& Other  
) _NOEXCEPT;  
```  
  
### Parameters  
 `Other`  
 A `unique_lock` object.  
  
### Return Value  
 `*this`  
  
### Remarks  
 If the calling thread owns the previously associated `mutex`, before this method calls `unlock` on the `mutex`, it assigns the new values.  
  
 After the copy, this method sets `Other` to a default-constructed state.  
  
##  <a name="unique_lock__owns_lock_method"></a>  unique_lock::owns_lock Method  
 Specifies whether the calling thread owns the associated `mutex`.  
  
```cpp  
bool owns_lock() const _NOEXCEPT;  
```  
  
### Return Value  
 `true` if the thread owns the `mutex`; otherwise, `false`.  
  
##  <a name="unique_lock__release_method"></a>  unique_lock::release Method  
 Disassociates the `unique_lock` object from the associated `mutex` object.  
  
```cpp  
mutex_type *release() _NOEXCEPT;  
```  
  
### Return Value  
 The previous value of the stored `mutex` pointer.  
  
### Remarks  
 This method sets the value of the stored `mutex` pointer to 0 and sets the internal `mutex` ownership flag to `false`.  
  
##  <a name="unique_lock__swap_method"></a>  unique_lock::swap Method  
 Swaps the associated `mutex` and ownership status with that of a specified object.  
  
```  
void swap(  
   unique_lock& Other  
) _NOEXCEPT;  
```  
  
### Parameters  
 `Other`  
 A `unique_lock` object.  
  
##  <a name="unique_lock__try_lock_method"></a>  unique_lock::try_lock Method  
 Attempts to obtain ownership of the associated `mutex` without blocking.  
  
```cpp  
bool try_lock() _NOEXCEPT;  
```  
  
### Return Value  
 `true` if the method successfully obtains ownership of the `mutex`; otherwise, `false`.  
  
### Remarks  
 If the stored `mutex` pointer is `null`, the method throws a [system_error](../vs140/system_error-Class.md) that has an error code of `operation_not_permitted`.  
  
 If the calling thread already owns the `mutex`, the method throws a `system_error` that has an error code of `resource_deadlock_would_occur`.  
  
##  <a name="unique_lock__try_lock_for_method"></a>  unique_lock::try_lock_for Method  
 Attempts to obtain ownership of the associated `mutex` without blocking.  
  
```  
template<class Rep,  
   class Period>  
bool try_lock_for(  
   const chrono::duration< Rep, Period>& Rel_time  
);  
```  
  
### Parameters  
 `Rel_time`  
 A [chrono::duration](../vs140/duration-Class.md) object that specifies the maximum amount of time that the method attempts to obtain ownership of the `mutex`.  
  
### Return Value  
 `true` if the method successfully obtains ownership of the `mutex`; otherwise, `false`.  
  
### Remarks  
 If the stored `mutex` pointer is `null`, the method throws a [system_error](../vs140/system_error-Class.md) that has an error code of `operation_not_permitted`.  
  
 If the calling thread already owns the `mutex`, the method throws a `system_error` that has an error code of `resource_deadlock_would_occur`.  
  
##  <a name="unique_lock__try_lock_until_method"></a>  unique_lock::try_lock_until Method  
 Attempts to obtain ownership of the associated `mutex` without blocking.  
  
```cpp  
template<class Clock, class Duration>  
   bool try_lock_until(const chrono::time_point<Clock, Duration>& Abs_time);  
bool try_lock_until(const xtime * Abs_time);  
```  
  
### Parameters  
 `Abs_time`  
 A point in time that specifies the threshold after which the method no longer attempts to obtain ownership of the `mutex`.  
  
### Return Value  
 `true` if the method successfully obtains ownership of the `mutex`; otherwise, `false`.  
  
### Remarks  
 If the stored `mutex` pointer is `null`, the method throws a [system_error](../vs140/system_error-Class.md) that has an error code of `operation_not_permitted`.  
  
 If the calling thread already owns the `mutex`, the method throws a `system_error` that has an error code of `resource_deadlock_would_occur`.  
  
##  <a name="unique_lock__unique_lock_constructor"></a>  unique_lock::unique_lock Constructor  
 Constructs a `unique_lock` object.  
  
```cpp  
unique_lock() noexcept;  
unique_lock(unique_lock&& Other) noexcept;  
explicit unique_lock(mutex_type& Mtx);  
unique_lock(mutex_type& Mtx, adopt_lock_t Adopt);  
unique_lock(mutex_type& Mtx, defer_lock_t Defer) noexcept;  
unique_lock(mutex_type& Mtx, try_to_lock_t Try);  
template<class Rep, class Period>  
   unique_lock(mutex_type& Mtx,  
      const chrono::duration<Rep, Period> Rel_time);  
template<class Clock, class Duration>  
   unique_lock(mutex_type& Mtx,  
      const chrono::time_point<Clock, Duration> Abs_time);  
unique_lock(mutex_type& Mtx,  
   const xtime * Abs_time) noexcept;  
```  
  
### Parameters  
 `Mtx`  
 A mutex type object.  
  
 `Rel_time`  
 A [chrono::duration](../vs140/duration-Class.md) object that specifies the maximum amount of time that the method attempts to obtain ownership of the `mutex`.  
  
 `Abs_time`  
 A point in time that specifies the threshold after which the method no longer attempts to obtain ownership of the `mutex`.  
  
 `Other`  
 A `unique_lock` object.  
  
### Remarks  
 The first constructor constructs an object that has an associated mutex pointer value of 0.  
  
 The second constructor moves the associated mutex status from `Other`. After the move, `Other` is no longer associated with a mutex.  
  
 The remaining constructors store & `Mtx` as the stored `mutex` pointer. Ownership of the `mutex` is determined by the second argument, if it exists.  
  
|||  
|-|-|  
|`No argument`|Ownership is obtained by calling the `lock` method on the associated `mutex` object.|  
|`Adopt`|Ownership is assumed. `Mtx` must be locked when the constructor is called.|  
|`Defer`|The calling thread is assumed not to own the `mutex` object. `Mtx` must not be locked when the constructor is called.|  
|`Try`|Ownership is determined by calling `try_lock` on the associated `mutex` object. The constructor throws nothing.|  
|`Rel_time`|Ownership is determined by calling `try_lock_for(Rel_time)`.|  
|`Abs_time`|Ownership is determined by calling `try_lock_until(Abs_time)`.|  
  
##  <a name="unique_lock___dtorunique_lock_destructor"></a>  unique_lock::~unique_lock Destructor  
 Releases any resources that are associated with the `unique_lock` object.  
  
```cpp  
~unique_lock() _NOEXCEPT;  
```  
  
### Remarks  
 If the calling thread owns the associated `mutex`, the destructor releases ownership by calling unlock on the `mutex` object.  
  
##  <a name="unique_lock__unlock_method"></a>  unique_lock::unlock Method  
 Releases ownership of the associated `mutex`.  
  
```cpp  
void unlock();  
```  
  
### Remarks  
 If the calling thread doesn't own the associated `mutex`, this method throws a [system_error](../vs140/system_error-Class.md) that has an error code of `operation_not_permitted`.  
  
 Otherwise, this method calls `unlock` on the associated `mutex` and sets the internal thread ownership flag to `false`.  
  
## See Also  
 [Header Files](../vs140/C---Standard-Library-Header-Files.md)   
 [<mutex\>](../vs140/-mutex-.md)