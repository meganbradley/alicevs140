---
title: "_freea"
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
  - _freea
apilocation: 
  - msvcr120.dll
  - msvcr110.dll
  - msvcr80.dll
  - msvcr90.dll
  - msvcr100.dll
  - msvcr110_clr0400.dll
  - msvcrt.dll
apitype: DLLExport
ms.assetid: dcd30584-dd9d-443b-8c4c-13237a1cecac
caps.latest.revision: 20
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _freea
Deallocates or frees a memory block.  
  
## Syntax  
  
```  
void _freea(   
   void *memblock   
);  
```  
  
#### Parameters  
 `memblock`  
 Previously allocated memory block to be freed.  
  
## Return Value  
 None.  
  
## Remarks  
 The `_freea` function deallocates a memory block (`memblock`) that was previously allocated by a call to [_malloca](../vs140/_malloca.md). `_freea` checks to see if the memory was allocated on the heap or the stack. If it was allocated on the stack, `_freea` does nothing. If it was allocated on the heap, the number of freed bytes is equivalent to the number of bytes requested when the block was allocated. If `memblock` is `NULL`, the pointer is ignored and `_freea` immediately returns. Attempting to free an invalid pointer (a pointer to a memory block that was not allocated by `_malloca`) might affect subsequent allocation requests and cause errors.  
  
 _`freea` calls `free` internally if it finds that the memory is allocated on the heap. Whether the memory is on the heap or the stack is determined by a marker placed in memory at the address immediately preceding the allocated memory.  
  
 If an error occurs in freeing the memory, `errno` is set with information from the operating system on the nature of the failure. For more information, see [_doserrno, errno, _sys_errlist, and _sys_nerr](../vs140/errno--_doserrno--_sys_errlist--and-_sys_nerr.md).  
  
 After a memory block has been freed, [_heapmin](../vs140/_heapmin.md) minimizes the amount of free memory on the heap by coalescing the unused regions and releasing them back to the operating system. Freed memory that is not released to the operating system is restored to the free pool and is available for allocation again.  
  
 A call to `_freea` must accompany all calls to `_malloca`. It is also an error to call `_freea` twice on the same memory. When the application is linked with a debug version of the C run-time libraries, particularly with [_malloc_dbg](../vs140/_malloc_dbg.md) features enabled by defining `_CRTDBG_MAP_ALLOC`, it is easier to find missing or duplicated calls to `_freea`. For more information about how the heap is managed during the debugging process, see [The CRT Debug Heap](../vs140/CRT-Debug-Heap-Details.md).  
  
 `_freea` is marked `__declspec(noalias)`, meaning that the function is guaranteed not to modify global variables. For more information, see [noalias](../vs140/noalias.md).  
  
## Requirements  
  
|Function|Required header|  
|--------------|---------------------|  
|`_freea`|<stdlib.h> and <malloc.h>|  
  
 For more compatibility information, see [Compatibility](../vs140/Compatibility.md) in the Introduction.  
  
## Example  
 See the example for [_malloca](../vs140/_malloca.md).  
  
## .NET Framework Equivalent  
 Not applicable. To call the standard C function, use `PInvoke`. For more information, see [Platform Invoke Examples](assetId:///15926806-f0b7-487e-93a6-4e9367ec689f).  
  
## See Also  
 [Memory Allocation](../vs140/Memory-Allocation.md)   
 [_malloca](../vs140/_malloca.md)   
 [calloc](../vs140/calloc.md)   
 [malloc](../vs140/malloc.md)   
 [_malloc_dbg](../vs140/_malloc_dbg.md)   
 [realloc](../vs140/realloc.md)   
 [_free_dbg](../vs140/_free_dbg.md)   
 [_heapmin](../vs140/_heapmin.md)