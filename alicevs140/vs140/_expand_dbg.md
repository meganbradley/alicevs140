---
title: "_expand_dbg"
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
  - _expand_dbg
apilocation: 
  - msvcr110.dll
  - msvcr110_clr0400.dll
  - msvcr80.dll
  - msvcr100.dll
  - msvcr120.dll
  - msvcrt.dll
  - msvcr90.dll
apitype: DLLExport
ms.assetid: dc58c91f-72a8-48c6-b643-fe130fb6c1fd
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _expand_dbg
Resizes a specified block of memory in the heap by expanding or contracting the block (debug version only).  
  
## Syntax  
  
```  
void *_expand_dbg(   
   void *userData,  
   size_t newSize,  
   int blockType,  
   const char *filename,  
   int linenumber   
);  
```  
  
#### Parameters  
 `userData`  
 Pointer to the previously allocated memory block.  
  
 `newSize`  
 Requested new size for the block (in bytes).  
  
 `blockType`  
 Requested type for resized block: `_CLIENT_BLOCK` or `_NORMAL_BLOCK`.  
  
 `filename`  
 Pointer to the name of the source file that requested expand operation or `NULL`.  
  
 `linenumber`  
 Line number in the source file where the expand operation was requested or `NULL`.  
  
 The `filename` and `linenumber` parameters are only available when `_expand_dbg` has been called explicitly or the [_CRTDBG_MAP_ALLOC](../vs140/_CRTDBG_MAP_ALLOC.md) preprocessor constant has been defined.  
  
## Return Value  
 On successful completion, `_expand_dbg` returns a pointer to the resized memory block. Because the memory is not moved, the address is the same as the userData. If an error occurred or the block could not be expanded to the requested size, it returns `NULL`. If a failure occurs, `errno` is with information from the operating system about the nature of the failure. For more information about `errno`, see [_doserrno, errno, _sys_errlist, and _sys_nerr](../vs140/errno--_doserrno--_sys_errlist--and-_sys_nerr.md).  
  
## Remarks  
 The `_expand_dbg` function is a debug version of the _[expand](../vs140/_expand.md) function. When [_DEBUG](../vs140/_DEBUG.md) is not defined, each call to `_expand_dbg` is reduced to a call to `_expand`. Both `_expand` and `_expand_dbg` resize a memory block in the base heap, but `_expand_dbg` accommodates several debugging features: buffers on either side of the user portion of the block to test for leaks, a block type parameter to track specific allocation types, and `filename`/`linenumber` information to determine the origin of allocation requests.  
  
 `_expand_dbg` resizes the specified memory block with slightly more space than the requested `newSize`. `newSize` might be greater or less than the size of the originally allocated memory block. The additional space is used by the debug heap manager to link the debug memory blocks and to provide the application with debug header information and overwrite buffers. The resize is accomplished by either expanding or contracting the original memory block. `_expand_dbg` does not move the memory block, as does the [_realloc_dbg](../vs140/_realloc_dbg.md) function.  
  
 When `newSize` is greater than the original block size, the memory block is expanded. During an expansion, if the memory block cannot be expanded to accommodate the requested size, `NULL` is returned. When `newSize` is less than the original block size, the memory block is contracted until the new size is obtained.  
  
 For information about how memory blocks are allocated, initialized, and managed in the debug version of the base heap, see [CRT Debug Heap Details](../vs140/CRT-Debug-Heap-Details.md). For information about the allocation block types and how they are used, see [Types of blocks on the debug heap](../vs140/CRT-Debug-Heap-Details.md#BKMK_Types_of_blocks_on_the_debug_heap). For information about the differences between calling a standard heap function and its debug version in a debug build of an application, see [Debug Versions of Heap Allocation Functions](../vs140/Debug-Versions-of-Heap-Allocation-Functions.md).  
  
 This function validates its parameters. If `memblock` is a null pointer, or if size is greater than `_HEAP_MAXREQ`, this function invokes an invalid parameter handler, as described in [Parameter Validation](../vs140/Parameter-Validation.md). If execution is allowed to continue, `errno` is set to `EINVAL` and the function returns `NULL`.  
  
## Requirements  
  
|Routine|Required header|  
|-------------|---------------------|  
|`_expand_dbg`|<crtdbg.h>|  
  
 For more compatibility information, see [Compatibility](../vs140/Compatibility.md).  
  
## Libraries  
 Debug versions of [C run-time libraries](../vs140/CRT-Library-Features.md) only.  
  
## Example  
  
```  
// crt_expand_dbg.c  
//  
// This program allocates a block of memory using _malloc_dbg  
// and then calls _msize_dbg to display the size of that block.  
// Next, it uses _expand_dbg to expand the amount of  
// memory used by the buffer and then calls _msize_dbg again to  
// display the new amount of memory allocated to the buffer.  
//  
  
#include <stdio.h>  
#include <malloc.h>  
#include <stdlib.h>  
#include <crtdbg.h>  
  
int main( void )  
{  
   long *buffer;  
   size_t size;  
  
   // Call _malloc_dbg to include the filename and line number  
   // of our allocation request in the header  
   buffer = (long *)_malloc_dbg( 40 * sizeof(long),  
                                 _NORMAL_BLOCK, __FILE__, __LINE__ );  
   if( buffer == NULL )  
      exit( 1 );  
  
   // Get the size of the buffer by calling _msize_dbg  
   size = _msize_dbg( buffer, _NORMAL_BLOCK );  
   printf( "Size of block after _malloc_dbg of 40 longs: %u\n", size );  
  
   // Expand the buffer using _expand_dbg and show the new size  
   buffer = (long *)_expand_dbg( buffer, size + sizeof(long),  
                                 _NORMAL_BLOCK, __FILE__, __LINE__ );  
  
   if( buffer == NULL )  
      exit( 1 );  
   size = _msize_dbg( buffer, _NORMAL_BLOCK );  
   printf( "Size of block after _expand_dbg of 1 more long: %u\n",  
           size );  
  
   free( buffer );  
   exit( 0 );  
}  
```  
  
 **Size of block after _malloc_dbg of 40 longs: 160**  
**Size of block after _expand_dbg of 1 more long: 164**   
## Comment  
 The output of this program depends on your computer's ability to expand all the sections. If all sections are expanded, the output is reflected in the Output section.  
  
## .NET Framework Equivalent  
 Not applicable. To call the standard C function, use `PInvoke`. For more information, see [Platform Invoke Examples](assetId:///15926806-f0b7-487e-93a6-4e9367ec689f).  
  
## See Also  
 [Debug Routines](../vs140/Debug-Routines.md)   
 [_malloc_dbg](../vs140/_malloc_dbg.md)