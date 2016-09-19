---
title: "Debug Versions of Heap Allocation Functions"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - FSharp
  - VB
  - CSharp
  - C++
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-debug
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 91748bdc-f4cd-4d8b-ab98-0493dab7ed0d
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Debug Versions of Heap Allocation Functions
The C run-time library contains special Debug versions of the heap allocation functions. These functions have the same names as the Release versions with _dbg appended to them. This topic describes the differences between the Release version of a CRT function and the _dbg version, using `malloc` and `_malloc_dbg` as examples.  
  
 When [_DEBUG](../vs140/_DEBUG.md) is defined, the CRT maps all [malloc](../vs140/malloc.md) calls to [_malloc_dbg](../vs140/_malloc_dbg.md). Therefore, you do not need to rewrite your code using `_malloc_dbg` instead of `malloc` to receive the benefits while debugging.  
  
 You might want to call `_malloc_dbg` explicitly, however. Calling `_malloc_dbg` explicitly has some added benefits:  
  
-   Tracking `_CLIENT_BLOCK` type allocations.  
  
-   Storing the source file and line number where the allocation request occurred.  
  
 If you do not want to convert your `malloc` calls to `_malloc_dbg`, you can obtain the source file information by defining [_CRTDBG_MAP_ALLOC](../vs140/_CRTDBG_MAP_ALLOC.md), which causes the preprocessor to directly map all calls to `malloc` to `_malloc_dbg` instead of relying on a wrapper around `malloc`.  
  
 To track the separate types of allocations in client blocks, you must call `_malloc_dbg` directly and set the `blockType` parameter to `_CLIENT_BLOCK`.  
  
 When _DEBUG is not defined, calls to `malloc` are not disturbed, calls to `_malloc_dbg` are resolved to `malloc`, the definition of [_CRTDBG_MAP_ALLOC](../vs140/_CRTDBG_MAP_ALLOC.md) is ignored, and source file information pertaining to the allocation request is not provided. Because `malloc` does not have a block type parameter, requests for `_CLIENT_BLOCK` types are treated as standard allocations.  
  
## See Also  
 [CRT Debugging Techniques](../vs140/CRT-Debugging-Techniques.md)