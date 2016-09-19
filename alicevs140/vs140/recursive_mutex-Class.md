---
title: "recursive_mutex Class"
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
ms.assetid: eb5ffd1b-7e78-4559-8391-bb220ead42fc
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# recursive_mutex Class
Represents a *mutex type*. In contrast to [mutex](../vs140/mutex-Class--STL-.md), the behavior of calls to locking methods for objects that are already locked is well-defined.  
  
## Syntax  
  
```  
class recursive_mutex;  
```  
  
## Members  
  
### Public Constructors  
  
|Name|Description|  
|----------|-----------------|  
|[recursive_mutex::recursive_mutex Constructor](#recursive_mutex__recursive_mutex_constructor)|Constructs a `recursive_mutex` object.|  
|[recursive_mutex::~recursive_mutex Destructor](#recursive_mutex___dtorrecursive_mutex_destructor)|Releases any resources that are used by the `recursive_mutex` object.|  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[recursive_mutex::lock Method](#recursive_mutex__lock_method)|Blocks the calling thread until the thread obtains ownership of the mutex.|  
|[recursive_mutex::try_lock Method](#recursive_mutex__try_lock_method)|Attempts to obtain ownership of the mutex without blocking.|  
|[recursive_mutex::unlock Method](#recursive_mutex__unlock_method)|Releases ownership of the mutex.|  
  
## Requirements  
 **Header:** mutex  
  
 **Namespace:** std  
  
##  <a name="recursive_mutex__lock_method"></a>  recursive_mutex::lock Method  
 Blocks the calling thread until the thread obtains ownership of the `mutex`.  
  
```cpp  
void lock();  
```  
  
### Remarks  
 If the calling thread already owns the `mutex`, the method returns immediately, and the previous lock remains in effect.  
  
##  <a name="recursive_mutex__recursive_mutex_constructor"></a>  recursive_mutex::recursive_mutex Constructor  
 Constructs a `recursive_mutex` object that is not locked.  
  
```cpp  
recursive_mutex();  
```  
  
##  <a name="recursive_mutex___dtorrecursive_mutex_destructor"></a>  recursive_mutex::~recursive_mutex Destructor  
 Releases any resources that are used by the object.  
  
```cpp  
~recursive_mutex();  
```  
  
### Remarks  
 If the object is locked when the destructor runs, the behavior is undefined.  
  
##  <a name="recursive_mutex__try_lock_method"></a>  recursive_mutex::try_lock Method  
 Attempts to obtain ownership of the `mutex` without blocking.  
  
```cpp  
bool try_lock() _NOEXCEPT;  
```  
  
### Return Value  
 `true` if the method successfully obtains ownership of the `mutex` or if the calling thread already owns the `mutex`; otherwise, `false`.  
  
### Remarks  
 If the calling thread already owns the `mutex`, the function immediately returns `true`, and the previous lock remains in effect.  
  
##  <a name="recursive_mutex__unlock_method"></a>  recursive_mutex::unlock Method  
 Releases ownership of the mutex.  
  
```cpp  
void unlock();  
```  
  
### Remarks  
 This method releases ownership of the `mutex` only after it is called as many times as [lock](#recursive_mutex__lock_method) and [try_lock](#recursive_mutex__try_lock_method) have been called successfully on the `recursive_mutex` object.  
  
 If the calling thread does not own the `mutex`, the behavior is undefined.  
  
## See Also  
 [Header Files](../vs140/C---Standard-Library-Header-Files.md)   
 [<mutex\>](../vs140/-mutex-.md)