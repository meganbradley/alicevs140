---
title: "_aligned_offset_realloc"
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
  - _aligned_offset_realloc
apilocation: 
  - msvcrt.dll
  - msvcr100.dll
  - msvcr80.dll
  - msvcr90.dll
  - msvcr110.dll
  - msvcr110_clr0400.dll
  - msvcr120.dll
apitype: DLLExport
ms.assetid: e0263533-991e-41b0-acc9-1b8a51ab9ecd
caps.latest.revision: 20
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _aligned_offset_realloc
Changes the size of a memory block that was allocated with [_aligned_malloc](../vs140/_aligned_malloc.md) or [_aligned_offset_malloc](../vs140/_aligned_offset_malloc.md).  
  
## Syntax  
  
```  
void * _aligned_offset_realloc(  
   void *memblock,   
   size_t size,   
   size_t alignment,  
   size_t offset  
);  
```  
  
#### Parameters  
 `memblock`  
 The current memory block pointer.  
  
 `size`  
 The size of the memory allocation.  
  
 `alignment`  
 The alignment value, which must be an integer power of 2.  
  
 `offset`  
 The offset into the memory allocation to force the alignment.  
  
## Return Value  
 `_aligned_offset_realloc` returns a void pointer to the reallocated (and possibly moved) memory block. The return value is `NULL` if the size is zero and the buffer argument is not `NULL`, or if there is not enough available memory to expand the block to the given size. In the first case, the original block is freed. In the second case, the original block is unchanged. The return value points to a storage space that is guaranteed to be suitably aligned for storage of any type of object. To get a pointer to a type other than void, use a type cast on the return value.  
  
 `_aligned_offset_realloc` is marked `__declspec(noalias)` and `__declspec(restrict)`, meaning that the function is guaranteed not to modify global variables and that the pointer returned is not aliased. For more information, see [noalias](../vs140/noalias.md) and [restrict](../vs140/restrict.md).  
  
## Remarks  
 Like [_aligned_offset_malloc](../vs140/_aligned_offset_malloc.md), `_aligned_offset_realloc` allows a structure to be aligned at an offset within the structure.  
  
 `_aligned_offset_realloc` is based on `malloc`. For more information about using `_aligned_offset_malloc`, see [malloc](../vs140/malloc.md). If `memblock` is `NULL`, the function calls `_aligned_offset_malloc` internally.  
  
 This function sets `errno` to `ENOMEM` if the memory allocation failed or if the requested size was greater than `_HEAP_MAXREQ`. For more information about `errno`, see [_doserrno, errno, _sys_errlist, and _sys_nerr](../vs140/errno--_doserrno--_sys_errlist--and-_sys_nerr.md). Also, `_aligned_offset_realloc` validates its parameters. If `alignment` is not a power of 2 or if `offset` is greater than or equal to `size` and nonzero, this function invokes the invalid parameter handler, as described in [Parameter Validation](../vs140/Parameter-Validation.md). If execution is allowed to continue, this function returns `NULL` and sets `errno` to `EINVAL`.  
  
## Requirements  
  
|Routine|Required header|  
|-------------|---------------------|  
|`_aligned_offset_realloc`|<malloc.h>|  
  
## Example  
 For more information, see [_aligned_malloc](../vs140/_aligned_malloc.md).  
  
## See Also  
 [Data Alignment](../vs140/Data-Alignment.md)