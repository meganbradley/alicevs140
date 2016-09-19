---
title: "future Class"
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
ms.assetid: 495e82c3-5341-4e37-87dd-b40107fbdfb6
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# future Class
Describes an *asynchronous return object*.  
  
## Syntax  
  
```  
template<class Ty>  
class future;  
```  
  
## Remarks  
 Each standard *asynchronous provider* returns an object whose type is an instantiation of this template. A `future` object provides the only access to the asynchronous provider that it is associated with. If you need multiple asynchronous return objects that are associated with the same asynchronous provider, copy the `future` object to a [shared_future](../vs140/shared_future-Class.md) object.  
  
## Members  
  
### Public Constructors  
  
|Name|Description|  
|----------|-----------------|  
|[future::future Constructor](#future__future_constructor)|Constructs a `future` object.|  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[future::get Method](#future__get_method)|Retrieves the result that is stored in the associated asynchronous state.|  
|[future::share Method](#future__share_method)|Converts the object to a `shared_future`.|  
|[future::valid Method](#future__valid_method)|Specifies whether the object is not empty.|  
|[future::wait Method](#future__wait_method)|Blocks the current thread until the associated asynchronous state is ready.|  
|[future::wait_for Method](#future__wait_for_method)|Blocks until the associated asynchronous state is ready or until the specified time has elapsed.|  
|[future::wait_until Method](#future__wait_until_method)|Blocks until the associated asynchronous state is ready or until a specified point in time.|  
  
### Public Operators  
  
|Name|Description|  
|----------|-----------------|  
|[future::operator= Operator](#future__operator_eq)|Transfers the associated asynchronous state from a specified object.|  
  
## Requirements  
 **Header:** future  
  
 **Namespace:** std  
  
##  <a name="future__future_constructor"></a>  future::future Constructor  
 Constructs a `future` object.  
  
```  
future() _NOEXCEPT;  
future(  
   future&& Other  
) _NOEXCEPT;  
  
```  
  
### Parameters  
 `Other`  
 A `future` object.  
  
### Remarks  
 The first constructor constructs a `future` object that has no associated asynchronous state.  
  
 The second constructor constructs a `future` object and transfers the associated asynchronous state from `Other`. `Other` no longer has an associated asynchronous state.  
  
##  <a name="future__get_method"></a>  future::get Method  
 Retrieves the result that is stored in the associated asynchronous state.  
  
```  
Ty get();  
```  
  
### Return Value  
 If the result is an exception, the method rethrows it. Otherwise, the result is returned.  
  
### Remarks  
 Before it retrieves the result, this method blocks the current thread until the associated asynchronous state is ready.  
  
 For the partial specialization `future<Ty&>`, the stored value is effectively a reference to the object that was passed to the asynchronous provider as the return value.  
  
 Because no stored value exists for the specialization `future<void>`, the method returns `void`.  
  
 In other specializations, the method moves its return value from the stored value. Therefore, call this method only once.  
  
##  <a name="future__operator_eq"></a>  future::operator=  
 Transfers an associated asynchronous state from a specified object.  
  
```  
future& operator=(  
   future&& Right  
) _NOEXCEPT;  
```  
  
### Parameters  
 `Right`  
 A `future` object.  
  
### Return Value  
 `*this`  
  
### Remarks  
 After the transfer, `Right` no longer has an associated asynchronous state.  
  
##  <a name="future__share_method"></a>  future::share Method  
 Converts the object to a [shared_future](../vs140/shared_future-Class.md) object.  
  
```  
shared_future<Ty> share();  
```  
  
### Return Value  
 `shared_future(move(*this))`  
  
##  <a name="future__valid_method"></a>  future::valid Method  
 Specifies whether the object has an associated asynchronous state.  
  
```  
bool valid() _NOEXCEPT;  
```  
  
### Return Value  
 `true` if the object has an associated asynchronous state; otherwise, `false`.  
  
##  <a name="future__wait_method"></a>  future::wait Method  
 Blocks the current thread until the associated asynchronous state is *ready*.  
  
```cpp  
void wait() const;  
```  
  
### Remarks  
 An associated asynchronous state is *ready* only if its asynchronous provider has stored a return value or stored an exception.  
  
##  <a name="future__wait_for_method"></a>  future::wait_for Method  
 Blocks the current thread until the associated asynchronous state is *ready* or until a specified time interval has elapsed.  
  
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
 An associated asynchronous state is ready only if its asynchronous provider has stored a return value or stored an exception.  
  
##  <a name="future__wait_until_method"></a>  future::wait_until Method  
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
 An associated asynchronous state is *ready* only if its asynchronous provider has stored a return value or stored an exception.  
  
## See Also  
 [Header Files](../vs140/C---Standard-Library-Header-Files.md)   
 [<future\>](../vs140/-future-.md)