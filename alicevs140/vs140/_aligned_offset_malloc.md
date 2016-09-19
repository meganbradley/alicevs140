---
title: "_aligned_offset_malloc"
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
  - _aligned_offset_malloc
apilocation: 
  - msvcr110_clr0400.dll
  - msvcrt.dll
  - msvcr90.dll
  - msvcr100.dll
  - msvcr110.dll
  - msvcr120.dll
  - msvcr80.dll
apitype: DLLExport
ms.assetid: 447681a3-7c95-4655-86ba-fa3a4ca4c521
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _aligned_offset_malloc
Allocates memory on a specified alignment boundary.  
  
## Syntax  
  
```  
void * _aligned_offset_malloc(  
   size_t size,   
   size_t alignment,   
   size_t offset  
);  
```  
  
#### Parameters  
 [in] `size`  
 The size of the requested memory allocation.  
  
 [in] `alignment`  
 The alignment value, which must be an integer power of 2.  
  
 [in] `offset`  
 The offset into the memory allocation to force the alignment.  
  
## Return Value  
 A pointer to the memory block that was allocated or `NULL` if the operation failed.  
  
## Remarks  
 `_aligned_offset_malloc` is useful in situations where alignment is needed on a nested element; for example, if alignment was needed on a nested class.  
  
 `_aligned_offset_malloc` is based on `malloc`; for more information, see [malloc](../vs140/malloc.md).  
  
 `_aligned_offset_malloc` is marked `__declspec(noalias)` and `__declspec(restrict)`, meaning that the function is guaranteed not to modify global variables and that the pointer returned is not aliased. For more information, see [noalias](../vs140/noalias.md) and [restrict](../vs140/restrict.md).  
  
 This function sets `errno` to `ENOMEM` if the memory allocation failed or if the requested size was greater than `_HEAP_MAXREQ`. For more information about `errno`, see [_doserrno, errno, _sys_errlist, and _sys_nerr](../vs140/errno--_doserrno--_sys_errlist--and-_sys_nerr.md). Also, `_aligned_offset_malloc` validates its parameters. If `alignment` is not a power of 2 or if `offset` is greater than or equal to `size` and nonzero, this function invokes the invalid parameter handler, as described in [Parameter Validation](../vs140/Parameter-Validation.md). If execution is allowed to continue, this function returns `NULL` and sets `errno` to `EINVAL`.  
  
## Requirements  
  
|Routine|Required header|  
|-------------|---------------------|  
|`_aligned_offset_malloc`|<malloc.h>|  
  
## Example  
 For more information, see [_aligned_malloc](../vs140/_aligned_malloc.md).  
  
## See Also  
 [Data Alignment](../vs140/Data-Alignment.md)