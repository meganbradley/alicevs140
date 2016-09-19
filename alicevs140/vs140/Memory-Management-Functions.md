---
title: "Memory Management Functions"
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
ms.assetid: d303dd2a-dfa4-4d90-a508-f6aa290bb9ea
caps.latest.revision: 7
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Memory Management Functions
This document describes the memory management functions that the Concurrency Runtime provides to help you allocate and free memory in a concurrent manner.  
  
> [!TIP]
>  The Concurrency Runtime provides a default scheduler, and therefore you are not required to create one in your application. Because the Task Scheduler helps you fine-tune the performance of your applications, we recommend that you start with the [Parallel Patterns Library (PPL)](../vs140/Parallel-Patterns-Library--PPL-.md) or the [Asynchronous Agents Library](../vs140/Asynchronous-Agents-Library.md) if you are new to the Concurrency Runtime.  
  
 The Concurrency Runtime provides two memory management functions that are optimized for allocating and freeing blocks of memory in a concurrent manner. The [concurrency::Alloc](../vs140/Alloc-Function.md) function allocates a block of memory by using the specified size. The [concurrency::Free](../vs140/Free-Function.md) function frees the memory that was allocated by `Alloc`.  
  
> [!NOTE]
>  The `Alloc` and `Free` functions rely on each other. Use the `Free` function only to release memory that you allocate by using the `Alloc` function. Also, when you use the `Alloc` function to allocate memory, use only the `Free` function to release that memory.  
  
 Use the `Alloc` and `Free` functions when you allocate and free a fixed set of allocation sizes from different threads or tasks. The Concurrency Runtime caches memory that it allocates from the C Runtime heap. The Concurrency Runtime holds a separate memory cache for each running thread; therefore, the runtime manages memory without the use of locks or memory barriers. An application benefits more from the `Alloc` and `Free` functions when the memory cache is accessed more frequently. For example, a thread that frequently calls both `Alloc` and `Free` benefits more than a thread that primarily calls `Alloc` or `Free`.  
  
> [!NOTE]
>  When you use these memory management functions, and your application uses lots of memory, the application may enter a low-memory condition sooner than you expect. Because the memory blocks that are cached by one thread are not available to any other thread, if one thread holds lots of memory, that memory is not available.  
  
## Example  
 For an example that uses the `Alloc` and `Free` functions to improve memory performance, see [How-to: Use Alloc and Free to Improve Memory Performance](../vs140/How-to--Use-Alloc-and-Free-to-Improve-Memory-Performance.md).  
  
## See Also  
 [Task Scheduler (Concurrency Runtime)](../vs140/Task-Scheduler--Concurrency-Runtime-.md)   
 [How-to: Use Alloc and Free to Improve Memory Performance](../vs140/How-to--Use-Alloc-and-Free-to-Improve-Memory-Performance.md)