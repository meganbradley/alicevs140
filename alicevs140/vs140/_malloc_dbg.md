---
title: "_malloc_dbg"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
  - C
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: article
apiname: 
  - _malloc_dbg
apilocation: 
  - msvcr110.dll
  - msvcr80.dll
  - msvcrt.dll
  - msvcr110_clr0400.dll
  - msvcr120.dll
  - msvcr90.dll
  - msvcr100.dll
apitype: DLLExport
ms.assetid: c97eca51-140b-4461-8bd2-28965b49ecdb
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _malloc_dbg
Allocates a block of memory in the heap with additional space for a debugging header and overwrite buffers (debug version only).  
  
## Syntax  
  
```  
void *_malloc_dbg(  
   size_t size,  
   int blockType,  
   const char *filename,  
   int linenumber   
);  
```  
  
#### Parameters  
 `size`  
 Requested size of the memory block (in bytes).  
  
 `blockType`  
 Requested type of the memory block: `_CLIENT_BLOCK` or `_NORMAL_BLOCK`.  
  
 `filename`  
 Pointer to the name of the source file that requested the allocation operation or NULL.  
  
 `linenumber`  
 Line number in the source file where the allocation operation was requested or NULL.  
  
 The `filename` and `linenumber` parameters are only available when `_malloc_dbg` has been called explicitly or the [_CRTDBG_MAP_ALLOC](../vs140/_CRTDBG_MAP_ALLOC.md) preprocessor constant has been defined.  
  
## Return Value  
 On successful completion, this function returns a pointer to the user portion of the allocated memory block, calls the new handler function, or returns NULL. For a complete description of the return behavior, see the following Remarks section. For more information about how the new handler function is used, see the [malloc](../vs140/malloc.md) function.  
  
## Remarks  
 `_malloc_dbg` is a debug version of the [malloc](../vs140/malloc.md) function. When [_DEBUG](../vs140/_DEBUG.md) is not defined, each call to `_malloc_dbg` is reduced to a call to `malloc`. Both `malloc` and `_malloc_dbg` allocate a block of memory in the base heap, but `_malloc_dbg` offers several debugging features: buffers on either side of the user portion of the block to test for leaks, a block type parameter to track specific allocation types, and `filename`/`linenumber` information to determine the origin of allocation requests.  
  
 `_malloc_dbg` allocates the memory block with slightly more space than the requested `size`. The additional space is used by the debug heap manager to link the debug memory blocks and to provide the application with debug header information and overwrite buffers. When the block is allocated, the user portion of the block is filled with the value 0xCD and each of the overwrite buffers are filled with 0xFD.  
  
 `_malloc_dbg` sets `errno` to `ENOMEM` if a memory allocation fails or if the amount of memory needed (including the overhead mentioned previously) exceeds `_HEAP_MAXREQ`. For information about this and other error codes, see [_doserrno, errno, _sys_errlist, and _sys_nerr](../vs140/errno--_doserrno--_sys_errlist--and-_sys_nerr.md).  
  
 For information about how memory blocks are allocated, initialized, and managed in the debug version of the base heap, see [CRT Debug Heap Details](../vs140/CRT-Debug-Heap-Details.md). For information about the allocation block types and how they are used, see [Types of Blocks on the Debug Heap](../vs140/CRT-Debug-Heap-Details.md#BKMK_Types_of_blocks_on_the_debug_heap). For information about the differences between calling a standard heap function and its debug version in a debug build of an application, see [Debug Versions of Heap Allocation Functions](../vs140/Debug-Versions-of-Heap-Allocation-Functions.md).  
  
## Requirements  
  
|Routine|Required header|  
|-------------|---------------------|  
|`_malloc_dbg`|<crtdbg.h>|  
  
 For more compatibility information, see [Compatibility](../vs140/Compatibility.md) in the Introduction.  
  
## Libraries  
 Debug versions of [C run-time libraries](../vs140/CRT-Library-Features.md) only.  
  
## Example  
 For a sample of how to use `_malloc_dbg`, see [crt_dbg1](assetId:///17b4b20c-e849-48f5-8eb5-dca6509cbaf9).  
  
## .NET Framework Equivalent  
 Not applicable. To call the standard C function, use `PInvoke`. For more information, see [Platform Invoke Examples](assetId:///15926806-f0b7-487e-93a6-4e9367ec689f).  
  
## See Also  
 [Debug Routines](../vs140/Debug-Routines.md)   
 [malloc](../vs140/malloc.md)   
 [_calloc_dbg](../vs140/_calloc_dbg.md)   
 [_calloc_dbg](../vs140/_calloc_dbg.md)