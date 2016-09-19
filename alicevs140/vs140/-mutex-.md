---
title: "&lt;mutex&gt;"
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
ms.assetid: efb60c89-687a-4e38-8fe4-694e11c4e8a3
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &lt;mutex&gt;
Include the standard header <mutex\> to define the classes `mutex`, `recursive_mutex`, `timed_mutex`, and `recursive_timed_mutex`; the templates `lock_guard` and `unique_lock`; and supporting types and functions that define mutual-exclusion code regions.  
  
> [!WARNING]
>  The STL synchronization types in Visual Studio 2015 are based on Windows synchronization primitives and no longer use ConcRT (except when the target platform is Windows XP). The types defined in <mutex\> should not be used with any ConcRT types or functions.  
  
## Syntax  
  
```cpp  
#include <mutex>  
```  
  
## Remarks  
  
> [!NOTE]
>  In code that is compiled by using **/clr** or **/clr:pure**, this header is blocked.  
  
 The classes `mutex` and `recursive_mutex` are *mutex types*. A mutex type has a default constructor and a destructor that does not throw exceptions. These objects have methods that provide mutual exclusion when multiple threads try to lock the same object. Specifically, a mutex type contains the methods `lock`, `try_lock`, and `unlock`:  
  
-   The `lock` method blocks the calling thread until the thread obtains ownership of the mutex. Its return value is ignored.  
  
-   The `try_lock` method tries to obtain ownership of the mutex without blocking. Its return type is convertible to `bool` and is `true` if the method obtains ownership, but is otherwise `false`.  
  
-   The `unlock` method releases the ownership of the mutex from the calling thread.  
  
 You can use mutex types as type arguments to instantiate the templates `lock_guard` and `unique_lock`. You can use objects of these types as the `Lock` argument to the wait member functions in the template [condition_variable_any](../vs140/condition_variable_any-Class.md).  
  
 A *timed mutex type* satisfies the requirements for a mutex type. In addition, it has the `try_lock_for` and `try_lock_until` methods that must be callable by using one argument and must return a type that is convertible to `bool`. A timed mutex type can define these functions by using additional arguments, provided that those additional arguments all have default values.  
  
-   The `try_lock_for` method must be callable by using one argument, `Rel_time`, whose type is an instantiation of [chrono::duration](../vs140/duration-Class.md). The method tries to obtain ownership of the mutex, but returns within the time that is designated by `Rel_time`, regardless of success. The return value converts to `true` if the method obtains ownership; otherwise, the return value converts to `false`.  
  
-   The `try_lock_until` method must be callable by using one argument, `Abs_time`, whose type is an instantiation of [chrono::time_point](../vs140/time_point-Class.md). The method tries to obtain ownership of the mutex, but returns no later than the time that is designated by `Abs_time`, regardless of success. The return value converts to `true` if the method obtains ownership; otherwise, the return value converts to `false`.  
  
 A mutex type is also known as a *lockable type*. If it does not provide the member function `try_lock`, it is a *basic lockable type*. A timed mutex type is also known as a *timed lockable type*.  
  
### Classes  
  
|Name|Description|  
|----------|-----------------|  
|[lock_guard Class](../vs140/lock_guard-Class.md)|Represents a template that can be instantiated to create an object whose destructor unlocks a `mutex`.|  
|[mutex Class](../vs140/mutex-Class--STL-.md)|Represents a mutex type. Use objects of this type to enforce mutual exclusion within a program.|  
|[recursive_mutex Class](../vs140/recursive_mutex-Class.md)|Represents a mutex type. In constrast to the `mutex` class, the behavior of calling locking methods for objects that are already locked is well-defined.|  
|[recursive_timed_mutex Class](../vs140/recursive_timed_mutex-Class.md)|Represents a timed mutex type. Use objects of this type to enforce mutual exclusion that has time-limited blocking within a program. Unlike objects of type `timed_mutex`, the effect of calling locking methods for `recursive_timed_mutex` objects is well-defined.|  
|[timed_mutex Class](../vs140/timed_mutex-Class.md)|Represents a timed mutex type. Use objects of this type to enforce mutual exclusion that has time-limited blocking within a program.|  
|[unique_lock Class](../vs140/unique_lock-Class.md)|Represents a template that can be instantiated to create objects that manage the locking and unlocking of a `mutex`.|  
  
### Functions  
  
|Name|Description|  
|----------|-----------------|  
|[call_once Function](../vs140/-mutex--functions.md#call_once_function)|Provides a mechanism for calling a specified callable object exactly once during execution.|  
|[lock Function](../vs140/-mutex--functions.md#lock_function)|Attempts to lock all arguments without deadlock.|  
  
### Structs  
  
|Name|Description|  
|----------|-----------------|  
|[adopt_lock_t Structure](../vs140/adopt_lock_t-Structure.md)|Represents a type that is used to define an `adopt_lock`.|  
|[defer_lock_t Structure](../vs140/defer_lock_t-Structure.md)|Represents a type that defines a `defer_lock` object that is used to select one of the overloaded constructors of `unique_lock`.|  
|[once_flag Structure](../vs140/once_flag-Structure.md)|Represents a `struct` that is used with the template function `call_once` to ensure that initialization code is called only once, even in the presence of multiple threads of execution.|  
|[try_to_lock_t Structure](../vs140/try_to_lock_t-Structure.md)|Represents a `struct` that defines a `try_to_lock` object and is used to select one of the overloaded constructors of `unique_lock`.|  
  
### Variables  
  
|Name|Description|  
|----------|-----------------|  
|[adopt_lock Variable](../vs140/-mutex--functions.md#adopt_lock_variable)|Represents an object that can be passed to constructors for `lock_guard` and `unique_lock` to indicate that the mutex object that is also being passed to the constructor is locked.|  
|[defer_lock Variable](../vs140/-mutex--functions.md#defer_lock_variable)|Represents an object that can be passed to the constructor for `unique_lock`, to indicate that the constructor should not lock the mutex object that is also being passed to it.|  
|[try_to_lock Variable](../vs140/-mutex--functions.md#try_to_lock_variable)|Represents an object that can be passed to the constructor for `unique_lock` to indicate that the constructor should try to unlock the `mutex` that is also being passed to it without blocking.|  
  
## See Also  
 [Header Files](../vs140/C---Standard-Library-Header-Files.md)