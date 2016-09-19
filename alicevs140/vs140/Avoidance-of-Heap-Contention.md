---
title: "Avoidance of Heap Contention"
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
ms.topic: reference
ms.assetid: 797129d7-5f8c-4b0e-8974-bb93217e9ab5
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Avoidance of Heap Contention
The default string managers provided by MFC and ATL are simple wrappers on top of a global heap. This global heap is fully thread-safe, meaning that multiple threads can allocate and free memory from it simultaneously without corrupting the heap. To help provide thread safety, the heap has to serialize access to itself. This is usually accomplished with a critical section or similar locking mechanism. Whenever two threads try to access the heap simultaneously, one thread is blocked until the other thread's request is finished. For many applications, this situation rarely occurs and the performance impact of the heap's locking mechanism is negligible. However, for applications that frequently access the heap from multiple threads contention for the heap's lock can cause the application to run slower than if it were single-threaded (even on machines with multiple CPUs).  
  
 Applications that use [CStringT](../vs140/CStringT-Class.md) are especially susceptible to heap contention because operations on `CStringT` objects frequently require reallocation of the string buffer.  
  
 One way to alleviate heap contention between threads is to have each thread allocate strings from a private, thread-local heap. As long as the strings allocated with a particular thread's allocator are used only in that thread, the allocator need not be thread-safe.  
  
## Example  
 The example below illustrates a thread procedure that allocates its own private non-thread-safe heap to use for strings on that thread:  
  
 [!CODE [NVC_ATLMFC_Utilities#182](../CodeSnippet/VS_Snippets_Cpp/NVC_ATLMFC_Utilities#182)]  
  
## Comments  
 Multiple threads could be running using this same thread procedure but since each thread has its own heap there is no contention between threads. In addition, the fact that each heap is not thread-safe gives a measurable increase in performance even if just one copy of the thread is running. This is the result of the heap not using expensive interlocked operations to protect against concurrent access.  
  
 For a more complicated thread procedure, it may be convenient to store a pointer to the thread's string manager in a thread local storage (TLS) slot. This allows other functions called by the thread procedure to access the thread's string manager.  
  
## See Also  
 [Memory Management with CStringT](../vs140/Memory-Management-with-CStringT.md)