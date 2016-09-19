---
title: "_recalloc"
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
  - _recalloc
apilocation: 
  - msvcr110_clr0400.dll
  - msvcrt.dll
  - msvcr110.dll
  - msvcr120.dll
  - msvcr100.dll
  - msvcr80.dll
  - msvcr90.dll
  - api-ms-win-crt-heap-l1-1-0.dll
  - msvcr120_clr0400.dll
apitype: DLLExport
ms.assetid: 1db8305a-3f03-418c-8844-bf9149f63046
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _recalloc
A combination of `realloc` and `calloc`. Reallocates an array in memory and initializes its elements to 0.  
  
## Syntax  
  
```  
void *_recalloc(   
   void *memblock  
   size_t num,  
   size_t size   
);  
```  
  
#### Parameters  
 `memblock`  
 Pointer to previously allocated memory block.  
  
 `num`  
 Number of elements.  
  
 `size`  
 Length in bytes of each element.  
  
## Return Value  
 `_recalloc` returns a `void` pointer to the reallocated (and possibly moved) memory block.  
  
 If there is not enough available memory to expand the block to the given size, the original block is left unchanged, and `NULL` is returned.  
  
 If the requested size is zero, then the block pointed to by `memblock` is freed; the return value is `NULL`, and `memblock` is left pointing at a freed block.  
  
 The return value points to a storage space that is guaranteed to be suitably aligned for storage of any type of object. To get a pointer to a type other than `void`, use a type cast on the return value.  
  
## Remarks  
 The _`recalloc` function changes the size of an allocated memory block. The `memblock` argument points to the beginning of the memory block. If `memblock` is `NULL`, \_`recalloc` behaves the same way as [calloc](../vs140/calloc.md) and allocates a new block of `num` * `size` bytes. Each element is initialized to 0. If `memblock` is not `NULL`, it should be a pointer returned by a previous call to `calloc`, [malloc](../vs140/malloc.md), or [realloc](../vs140/realloc.md).  
  
 Because the new block can be in a new memory location, the pointer returned by _`recalloc` is not guaranteed to be the pointer passed through the `memblock` argument.  
  
 `_recalloc` sets `errno` to `ENOMEM` if the memory allocation fails or if the amount of memory requested exceeds `_HEAP_MAXREQ`. For information on this and other error codes, see [_doserrno, errno, _sys_errlist, and _sys_nerr](../vs140/errno--_doserrno--_sys_errlist--and-_sys_nerr.md).  
  
 `recalloc` calls `realloc` in order to use the C++ [_set_new_mode](../vs140/_set_new_mode.md) function to set the new handler mode. The new handler mode indicates whether, on failure, `realloc` is to call the new handler routine as set by [_set_new_handler](../vs140/_set_new_handler.md). By default, `realloc` does not call the new handler routine on failure to allocate memory. You can override this default behavior so that, when _`recalloc` fails to allocate memory, `realloc` calls the new handler routine in the same way that the `new` operator does when it fails for the same reason. To override the default, call  
  
```  
_set_new_mode(1)  
```  
  
 early in the program, or link with NEWMODE.OBJ.  
  
 When the application is linked with a debug version of the C run-time libraries, _`recalloc` resolves to [_recalloc_dbg](../vs140/_recalloc_dbg.md). For more information about how the heap is managed during the debugging process, see [The CRT Debug Heap](../vs140/CRT-Debug-Heap-Details.md).  
  
 `_recalloc` is marked `__declspec(noalias)` and `__declspec(restrict)`, meaning that the function is guaranteed not to modify global variables, and that the pointer returned is not aliased. For more information, see [noalias](../vs140/noalias.md) and [restrict](../vs140/restrict.md).  
  
## Requirements  
  
|Routine|Required header|  
|-------------|---------------------|  
|`_recalloc`|<stdlib.h> and <malloc.h>|  
  
 For additional compatibility information, see [Compatibility](../vs140/Compatibility.md) in the Introduction.  
  
## .NET Framework Equivalent  
 Not applicable. To call the standard C function, use `PInvoke`. For more information, see [Platform Invoke Examples](assetId:///15926806-f0b7-487e-93a6-4e9367ec689f).  
  
## See Also  
 [Memory Allocation](../vs140/Memory-Allocation.md)   
 [_recalloc_dbg](../vs140/_recalloc_dbg.md)   
 [_aligned_recalloc](../vs140/_aligned_recalloc.md)   
 [_aligned_offset_recalloc](../vs140/_aligned_offset_recalloc.md)   
 [free](../vs140/free.md)   
 [Link options](../vs140/Link-Options.md)