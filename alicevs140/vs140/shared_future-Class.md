---
title: "shared_future Class"
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
ms.assetid: 454ebedd-f42b-405f-99a5-a25cc9ad7c90
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# shared_future Class
Describes an *asynchronous return object*. In contrast with a [future](../vs140/future-Class.md) object, an *asynchronous provider* can be associated with any number of `shared_future` objects.  
  
## Syntax  
  
```  
template<class Ty>  
class shared_future;  
```  
  
## Remarks  
 Do not call any methods other than `valid`, `operator=`, and the destructor on a `shared_future` object that's *empty*.  
  
 `shared_future` objects are not synchronized. Calling methods on the same object from multiple threads introduces a data race that has unpredictable results.  
  
## Members  
  
### Public Constructors  
  
|Name|Description|  
|----------|-----------------|  
|[shared_future::shared_future Constructor](#shared_future__shared_future_constructor)|Constructs a `shared_future` object.|  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[shared_future::get Method](#shared_future__get_method)|Retrieves the result that's stored in the *associated asynchronous state*.|  
|[shared_future::valid Method](#shared_future__valid_method)|Specifies whether the object is not empty.|  
|[shared_future::wait Method](#shared_future__wait_method)|Blocks the current thread until the associated asynchronous state is ready.|  
|[shared_future::wait_for Method](#shared_future__wait_for_method)|Blocks until the associated asynchronous state is ready or until the specified time has elapsed.|  
|[shared_future::wait_until Method](#shared_future__wait_until_method)|Blocks until the associated asynchronous state is ready or until a specified point in time.|  
  
### Public Operators  
  
|Name|Description|  
|----------|-----------------|  
|[shared_future::operator= Operator](#shared_future__operator_eq)|Assigns a new associated asynchronous state.|  
  
## Requirements  
 **Header:** future  
  
 **Namespace:** std  
  
##  <a name="shared_future__get_method"></a>  shared_future::get Method  
 Retrieves the result that's stored in the *associated asynchronous state*.  
  
```  
const Ty& get() const;  
Ty& get() const;  
void get() const;  
```  
  
### Remarks  
 If the result is an exception, the method rethrows it. Otherwise, the result is returned.  
  
 Before it retrieves the result, this method blocks the current thread until the associated asynchronous state is ready.  
  
 For the partial specialization `shared_future<Ty&>`, the stored value is effectively a reference to the object that was passed to the *asynchronous provider* as the return value.  
  
 Because no stored value exists for the specialization `shared_future<void>`, the method returns `void`.  
  
##  <a name="shared_future__operator_eq"></a>  shared_future::operator=  
 Transfers an *associated asynchronous state* from a specified object.  
  
```  
shared_future& operator=(shared_future&& Right) noexcept;  
shared_future& operator=(const shared_future& Right);  
```  
  
### Parameters  
 `Right`  
 A `shared_future` object.  
  
### Return Value  
 `*this`  
  
### Remarks  
 For the first operator, `Right` no longer has an associated asynchronous state after the operation.  
  
 For the second method, `Right` maintains its associated asynchronous state.  
  
##  <a name="shared_future__shared_future_constructor"></a>  shared_future::shared_future Constructor  
 Constructs a `shared_future` object.  
  
```  
shared_future() _NOEXCEPT;  
shared_future(future<Ty>&& Right) _NOEXCEPT;  
shared_future(shared_future&& Right) _NOEXCEPT;  
shared_future(const shared_future& Right);  
```  
  
### Parameters  
 `Right`  
 A [future](../vs140/future-Class.md) or `shared_future` object.  
  
### Remarks  
 The first constructor constructs a `shared_future` object that has no *associated asynchronous state*.  
  
 The second and third constructors construct a `shared_future` object and transfer the associated asynchronous state from `Right`. `Right` no longer has an associated asynchronous state.  
  
 The fourth constructor constructs a `shared_future` object that has the same associated asynchronous state as `Right`.  
  
##  <a name="shared_future__valid_method"></a>  shared_future::valid Method  
 Specifies whether the object has an *associated asynchronous state*.  
  
```  
bool valid() _NOEXCEPT;  
```  
  
### Return Value  
 `true` if the object has an associated asynchronous state; otherwise, `false`.  
  
##  <a name="shared_future__wait_method"></a>  shared_future::wait Method  
 Blocks the current thread until the *associated asynchronous state* is *ready*.  
  
```cpp  
void wait() const;  
```  
  
### Remarks  
 An associated asynchronous state is ready only if its asynchronous provider has stored a return value or stored an exception.  
  
##  <a name="shared_future__wait_for_method"></a>  shared_future::wait_for Method  
 Blocks the current thread until the associated asynchronous state is *ready* or until a specified time has elapsed.  
  
```cpp  
template<class Rep, class Period>  
   future_status wait_for(  
      const chrono::duration<Rep, Period>& Rel_time) const;  
```  
  
### Parameters  
 `Rel_time`  
 A [chrono::duration](../vs140/duration-Class.md) object that specifies a maximum time interval that the thread blocks.  
  
### Return Value  
 A [future_status](../vs140/-future--enums.md#future_status_enumeration) that indicates the reason for returning.  
  
### Remarks  
 An associated asynchronous state is *ready* only if its asynchronous provider has stored a return value or stored an exception.  
  
##  <a name="shared_future__wait_until_method"></a>  shared_future::wait_until Method  
 Blocks the current thread until the associated asynchronous state is *ready* or until after a specified time point.  
  
```cpp  
template<class Clock, class Duration>  
   future_status wait_until(  
      const chrono::time_point<Clock, Duration>& Abs_time) const;  
```  
  
### Parameters  
 `Abs_time`  
 A [chrono::time_point](../vs140/time_point-Class.md) object that specifies a time after which the thread can unblock.  
  
### Return Value  
 A [future_status](../vs140/-future--enums.md#future_status_enumeration) that indicates the reason for returning.  
  
### Remarks  
 An associated asynchronous state is ready only if its asynchronous provider has stored a return value or stored an exception.  
  
## See Also  
 [Header Files](../vs140/C---Standard-Library-Header-Files.md)   
 [<future\>](../vs140/-future-.md)