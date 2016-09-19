---
title: "Synchronization Data Structures"
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
ms.assetid: d612757d-e4b7-4019-a627-f853af085b8b
caps.latest.revision: 27
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Synchronization Data Structures
The Concurrency Runtime provides several data structures that let you synchronize access to shared data from multiple threads. These data structures are useful when you have shared data that you modify infrequently. A synchronization object, for example, a critical section, causes other threads to wait until the shared resource is available. Therefore, if you use such an object to synchronize access to data that is used frequently, you can lose scalability in your application. The [Parallel Patterns Library (PPL)](../vs140/Parallel-Patterns-Library--PPL-.md) provides the [concurrency::combinable](../vs140/combinable-Class.md) class, which enables you to share a resource among several threads or tasks without the need for synchronization. For more information about the `combinable` class, see [Parallel Containers and Objects](../vs140/Parallel-Containers-and-Objects.md).  
  
##  <a name="top"></a> Sections  
 This topic describes the following asynchronous message block types in detail:  
  
-   [critical_section](#critical_section)  
  
-   [reader_writer_lock](#reader_writer_lock)  
  
-   [scoped_lock and scoped_lock_read](#scoped_lock)  
  
-   [event](#event)  
  
##  <a name="critical_section"></a> critical_section  
 The [concurrency::critical_section](../vs140/critical_section-Class.md) class represents a cooperative mutual exclusion object that yields to other tasks instead of preempting them. Critical sections are useful when multiple threads require exclusive read and write access to shared data.  
  
 The `critical_section` class is non-reentrant. The [concurrency::critical_section::lock](../vs140/critical_section--lock-Method.md) method throws an exception of type [concurrency::improper_lock](../vs140/improper_lock-Class.md) if it is called by the thread that already owns the lock.  
  
### Methods and Features  
 The following table shows the important methods that are defined by the `critical_section` class.  
  
|Method|Description|  
|------------|-----------------|  
|[lock](../vs140/critical_section--lock-Method.md)|Acquires the critical section. The calling context blocks until it acquires the lock.|  
|[try_lock](../vs140/critical_section--try_lock-Method.md)|Tries to acquire the critical section, but does not block.|  
|[unlock](../vs140/critical_section--unlock-Method.md)|Releases the critical section.|  
  
 [[Top](#top)]  
  
##  <a name="reader_writer_lock"></a> reader_writer_lock  
 The [concurrency::reader_writer_lock](../vs140/reader_writer_lock-Class.md) class provides thread-safe read/write operations to shared data. Use reader/writer locks when multiple threads require concurrent read access to a shared resource but rarely write to that shared resource. This class gives only one thread write access to an object at any time.  
  
 The `reader_writer_lock` class can perform better than the `critical_section` class because a `critical_section` object acquires exclusive access to a shared resource, which prevents concurrent read access.  
  
 Like the `critical_section` class, the `reader_writer_lock` class represents a cooperative mutual exclusion object that yields to other tasks instead of preempting them.  
  
 When a thread that must write to a shared resource acquires a reader/writer lock, other threads that also must access the resource are blocked until the writer releases the lock. The `reader_writer_lock` class is an example of a *write-preference* lock, which is a lock that unblocks waiting writers before it unblocks waiting readers.  
  
 Like the `critical_section` class, the `reader_writer_lock` class is non-reentrant. The [concurrency::reader_writer_lock::lock](../vs140/reader_writer_lock--lock-Method.md) and [concurrency::reader_writer_lock::lock_read](../vs140/reader_writer_lock--lock_read-Method.md) methods throw an exception of type `improper_lock` if they are called by a thread that already owns the lock.  
  
> [!NOTE]
>  Because the `reader_writer_lock` class is non-reentrant, you cannot upgrade a read-only lock to a reader/writer lock or downgrade a reader/writer lock to a read-only lock. Performing either of these operations produces unspecified behavior.  
  
### Methods and Features  
 The following table shows the important methods that are defined by the `reader_writer_lock` class.  
  
|Method|Description|  
|------------|-----------------|  
|[lock](../vs140/reader_writer_lock--lock-Method.md)|Acquires read/write access to the lock.|  
|[try_lock](../vs140/reader_writer_lock--try_lock-Method.md)|Tries to acquire read/write access to the lock, but does not block.|  
|[lock_read](../vs140/reader_writer_lock--lock_read-Method.md)|Acquires read-only access to the lock.|  
|[try_lock_read](../vs140/reader_writer_lock--try_lock_read-Method.md)|Tries to acquire read-only access to the lock, but does not block.|  
|[unlock](../vs140/reader_writer_lock--unlock-Method.md)|Releases the lock.|  
  
 [[Top](#top)]  
  
##  <a name="scoped_lock"></a> scoped_lock and scoped_lock_read  
 The `critical_section` and `reader_writer_lock` classes provide nested helper classes that simplify the way you work with mutual exclusion objects. These helper classes are known as *scoped locks*.  
  
 The `critical_section` class contains the [concurrency::critical_section::scoped_lock](../vs140/critical_section--scoped_lock-Class.md) class. The constructor acquires access to the provided `critical_section` object; the destructor releases access to that object. The `reader_writer_lock` class contains the [concurrency::reader_writer_lock::scoped_lock](../vs140/reader_writer_lock--scoped_lock-Class.md) class, which resembles `critical_section::scoped_lock`, except that it manages write access to the provided `reader_writer_lock` object. The `reader_writer_lock` class also contains the [concurrency::reader_writer_lock::scoped_lock_read](../vs140/reader_writer_lock--scoped_lock_read-Class.md) class. This class manages read access to the provided `reader_writer_lock` object.  
  
 Scoped locks provide several benefits when you are working with `critical_section` and `reader_writer_lock` objects manually. Typically, you allocate a scoped lock on the stack. A scoped lock releases access to its mutual exclusion object automatically when it is destroyed; therefore, you do not manually unlock the underlying object. This is useful when a function contains multiple `return` statements. Scoped locks can also help you write exception-safe code. When a `throw` statement causes the stack to unwind, the destructor for any active scoped lock is called, and therefore the mutual exclusion object is always correctly released.  
  
> [!NOTE]
>  When you use the `critical_section::scoped_lock`, `reader_writer_lock::scoped_lock`, and `reader_writer_lock::scoped_lock_read` classes, do not manually release access to the underlying mutual exclusion object. This can put the runtime in an invalid state.  
  
##  <a name="event"></a> event  
 The [concurrency::event](../vs140/event-Class.md) class represents a synchronization object whose state can be signaled or non-signaled. Unlike synchronization objects, such as critical sections, whose purpose is to protect access to shared data, events synchronize flow of execution.  
  
 The `event` class is useful when one task has completed work for another task. For example, one task might signal another task that it has read data from a network connection or from a file.  
  
### Methods and Features  
 The following table shows several of the important methods that are defined by the `event` class.  
  
|Method|Description|  
|------------|-----------------|  
|[wait](../vs140/event--wait-Method.md)|Waits for the event to become signaled.|  
|[set](../vs140/event--set-Method.md)|Sets the event to the signaled state.|  
|[reset](../vs140/event--reset-Method.md)|Sets the event to the non-signaled state.|  
|[wait_for_multiple](../vs140/event--wait_for_multiple-Method.md)|Waits for multiple events to become signaled.|  
  
### Example  
 For an example that shows how to use the `event` class, see [Comparing Synchronization Data Structures to the Windows API](../vs140/Comparing-Synchronization-Data-Structures-to-the-Windows-API.md).  
  
 [[Top](#top)]  
  
## Related Sections  
 [Comparing Synchronization Data Structures to the Windows API](../vs140/Comparing-Synchronization-Data-Structures-to-the-Windows-API.md)  
 Compares the behavior of the synchronization data structures to those provided by the Windows API.  
  
 [Concurrency Runtime](../vs140/Concurrency-Runtime.md)  
 Describes the Concurrency Runtime, which simplifies parallel programming, and contains links to related topics.