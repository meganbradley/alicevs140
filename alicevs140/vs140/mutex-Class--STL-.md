---
title: "mutex Class (STL)"
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
ms.assetid: 7999d055-f74f-4303-810f-8d3c9cde2f69
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# mutex Class (STL)
Represents a *mutex type*. Objects of this type can be used to enforce mutual exclusion within a program.  
  
## Syntax  
  
```  
class mutex;  
```  
  
## Members  
  
### Public Constructors  
  
|Name|Description|  
|----------|-----------------|  
|[mutex::mutex Constructor (STL)](#mutex__mutex_constructor)|Constructs a `mutex` object.|  
|[mutex::~mutex Destructor (STL)](#mutex___dtormutex_destructor)|Releases any resources that were used by the `mutex` object.|  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[mutex::lock Method (STL)](#mutex__lock_method)|Blocks the calling thread until the thread obtains ownership of the `mutex`.|  
|[mutex::native_handle Method](#mutex__native_handle_method)|Returns the implementation-specific type that represents the mutex handle.|  
|[mutex::try_lock method (STL)](#mutex__try_lock_method)|Attempts to obtain ownership of the `mutex` without blocking.|  
|[mutex::unlock Method (STL)](#mutex__unlock_method)|Releases ownership of the `mutex`.|  
  
## Requirements  
 **Header:** mutex  
  
 **Namespace:** std  
  
##  <a name="mutex__lock_method"></a>  mutex::lock Method  
 Blocks the calling thread until the thread obtains ownership of the `mutex`.  
  
```cpp  
void lock();  
```  
  
### Remarks  
 If the calling thread already owns the `mutex`, the behavior is undefined.  
  
##  <a name="mutex__mutex_constructor"></a>  mutex::mutex Constructor  
 Constructs a `mutex` object that is not locked.  
  
```cpp  
constexpr mutex() _NOEXCEPT;  
```  
  
##  <a name="mutex___dtormutex_destructor"></a>  mutex::~mutex Destructor  
 Releases any resources that are used by the `mutex` object.  
  
```cpp  
~mutex();  
```  
  
### Remarks  
 If the object is locked when the destructor runs, the behavior is undefined.  
  
##  <a name="mutex__native_handle_method"></a>  mutex::native_handle Method  
 Returns the implementation-specific type that represents the mutex handle. The mutex handle can be used in implementation-specific ways.  
  
```  
native_handle_type native_handle();  
```  
  
### Return Value  
 `native_handle_type` is defined as a `Concurrency::critical_section *` that's cast as `void *`.  
  
##  <a name="mutex__try_lock_method"></a>  mutex::try_lock Method  
 Attempts to obtain ownership of the `mutex` without blocking.  
  
```cpp  
bool try_lock();  
```  
  
### Return Value  
 `true` if the method successfully obtains ownership of the `mutex`; otherwise, `false`.  
  
### Remarks  
 If the calling thread already owns the `mutex`, the behavior is undefined.  
  
##  <a name="mutex__unlock_method"></a>  mutex::unlock Method  
 Releases ownership of the `mutex`.  
  
```cpp  
void unlock();  
```  
  
### Remarks  
 If the calling thread does not own the `mutex`, the behavior is undefined.  
  
## See Also  
 [Header Files](../vs140/C---Standard-Library-Header-Files.md)   
 [<mutex\>](../vs140/-mutex-.md)