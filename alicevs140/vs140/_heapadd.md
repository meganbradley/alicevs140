---
title: "_heapadd"
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
  - _heapadd
apilocation: 
  - msvcr100.dll
  - msvcr110_clr0400.dll
  - msvcr120.dll
  - msvcr80.dll
  - msvcrt.dll
  - msvcr110.dll
  - msvcr90.dll
apitype: DLLExport
ms.assetid: 4d691fe2-2763-49f4-afb1-62738b7cd3ff
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _heapadd
Adds memory to the heap.  
  
> [!IMPORTANT]
>  This function is obsolete. Beginning in Visual Studio 2015, it is not available in the CRT.  
  
## Syntax  
  
```  
int _heapadd(   
   void *memblock,  
   size_t size   
);  
```  
  
#### Parameters  
 `memblock`  
 Pointer to the heap memory.  
  
 `size`  
 Size of memory to add, in bytes.  
  
## Return Value  
 If successful, `_heapadd` returns 0; otherwise, the function returns –1 and sets `errno` to `ENOSYS`.  
  
 For more information about this and other return codes, see [_doserrno, errno, _sys_errlist, and _sys_nerr](../vs140/errno--_doserrno--_sys_errlist--and-_sys_nerr.md).  
  
## Remarks  
 Beginning with Visual C++ version 4.0, the underlying heap structure was moved to the C run-time libraries to support the new debugging features. As a result, `_heapadd` is no longer supported on any platform that is based on the Win32 API.  
  
## Requirements  
  
|Routine|Required header|Optional header|  
|-------------|---------------------|---------------------|  
|`_heapadd`|<malloc.h>|<errno.h>|  
  
 For more compatibility information, see [Compatibility](../vs140/Compatibility.md) in the Introduction.  
  
## .NET Framework Equivalent  
 Not applicable. To call the standard C function, use `PInvoke`. For more information, see [Platform Invoke Examples](assetId:///15926806-f0b7-487e-93a6-4e9367ec689f).  
  
## See Also  
 [Memory Allocation](../vs140/Memory-Allocation.md)   
 [free](../vs140/free.md)   
 [_heapchk](../vs140/_heapchk.md)   
 [_heapmin](../vs140/_heapmin.md)   
 [_heapset](../vs140/_heapset.md)   
 [_heapwalk](../vs140/_heapwalk.md)   
 [malloc](../vs140/malloc.md)   
 [realloc](../vs140/realloc.md)