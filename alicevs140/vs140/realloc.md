---
title: "realloc"
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
  - realloc
apilocation: 
  - msvcr110.dll
  - msvcr120.dll
  - msvcrt.dll
  - msvcr100.dll
  - msvcr110_clr0400.dll
  - msvcr90.dll
  - msvcr80.dll
  - msvcr120_clr0400.dll
apitype: DLLExport
ms.assetid: 2b2239de-810b-4b11-9438-32ab0a244185
caps.latest.revision: 20
translation.priority.ht: 
  - de-de
  - ja-jp
---
# realloc
Reallocate memory blocks.  
  
## Syntax  
  
```  
void *realloc(  
   void *memblock,  
   size_t size   
);  
```  
  
#### Parameters  
 `memblock`  
 Pointer to previously allocated memory block.  
  
 `size`  
 New size in bytes.  
  
## Return Value  
 `realloc` returns a `void` pointer to the reallocated (and possibly moved) memory block.  
  
 If there is not enough available memory to expand the block to the given size, the original block is left unchanged, and `NULL` is returned.  
  
 If `size` is zero, then the block pointed to by `memblock` is freed; the return value is `NULL`, and `memblock` is left pointing at a freed block.  
  
 The return value points to a storage space that is guaranteed to be suitably aligned for storage of any type of object. To get a pointer to a type other than `void`, use a type cast on the return value.  
  
## Remarks  
 The `realloc` function changes the size of an allocated memory block. The `memblock` argument points to the beginning of the memory block. If `memblock` is `NULL`, `realloc` behaves the same way as `malloc` and allocates a new block of `size` bytes. If `memblock` is not `NULL`, it should be a pointer returned by a previous call to `calloc`, `malloc`, or `realloc`.  
  
 The `size` argument gives the new size of the block, in bytes. The contents of the block are unchanged up to the shorter of the new and old sizes, although the new block can be in a different location. Because the new block can be in a new memory location, the pointer returned by `realloc` is not guaranteed to be the pointer passed through the `memblock` argument. `realloc` does not zero newly allocated memory in the case of buffer growth.  
  
 `realloc` sets `errno` to `ENOMEM` if the memory allocation fails or if the amount of memory requested exceeds `_HEAP_MAXREQ`. For information on this and other error codes, see [_doserrno, errno, _sys_errlist, and _sys_nerr](../vs140/errno--_doserrno--_sys_errlist--and-_sys_nerr.md).  
  
 `realloc` calls `malloc`in order to use the C++ [_set_new_mode](../vs140/_set_new_mode.md) function to set the new handler mode. The new handler mode indicates whether, on failure, `malloc` is to call the new handler routine as set by [_set_new_handler](../vs140/_set_new_handler.md). By default, `malloc` does not call the new handler routine on failure to allocate memory. You can override this default behavior so that, when `realloc` fails to allocate memory, `malloc` calls the new handler routine in the same way that the `new` operator does when it fails for the same reason. To override the default, call  
  
```  
_set_new_mode(1)  
```  
  
 early in ones program, or link with NEWMODE.OBJ (see [Link Options](../vs140/Link-Options.md)).  
  
 When the application is linked with a debug version of the C run-time libraries, `realloc` resolves to [_realloc_dbg](../vs140/_realloc_dbg.md). For more information about how the heap is managed during the debugging process, see [The CRT Debug Heap](../vs140/CRT-Debug-Heap-Details.md).  
  
 `realloc` is marked `__declspec(noalias)` and `__declspec(restrict)`, meaning that the function is guaranteed not to modify global variables, and that the pointer returned is not aliased. For more information, see [noalias](../vs140/noalias.md) and [restrict](../vs140/restrict.md).  
  
## Requirements  
  
|Routine|Required header|  
|-------------|---------------------|  
|`realloc`|<stdlib.h> and <malloc.h>|  
  
 For additional compatibility information, see [Compatibility](../vs140/Compatibility.md) in the Introduction.  
  
## Example  
  
```  
// crt_realloc.c  
// This program allocates a block of memory for  
// buffer and then uses _msize to display the size of that  
// block. Next, it uses realloc to expand the amount of  
// memory used by buffer and then calls _msize again to  
// display the new amount of memory allocated to buffer.  
  
#include <stdio.h>  
#include <malloc.h>  
#include <stdlib.h>  
  
int main( void )  
{  
   long *buffer, *oldbuffer;  
   size_t size;  
  
   if( (buffer = (long *)malloc( 1000 * sizeof( long ) )) == NULL )  
      exit( 1 );  
  
   size = _msize( buffer );  
   printf_s( "Size of block after malloc of 1000 longs: %u\n", size );  
  
   // Reallocate and show new size:  
   oldbuffer = buffer;     // save pointer in case realloc fails  
   if( (buffer = realloc( buffer, size + (1000 * sizeof( long )) ))   
        ==  NULL )  
   {  
      free( oldbuffer );  // free original block  
      exit( 1 );  
   }  
   size = _msize( buffer );  
   printf_s( "Size of block after realloc of 1000 more longs: %u\n",   
            size );  
  
   free( buffer );  
   exit( 0 );  
}  
```  
  
 **Size of block after malloc of 1000 longs: 4000**  
**Size of block after realloc of 1000 more longs: 8000**   
## .NET Framework Equivalent  
 Not applicable. To call the standard C function, use `PInvoke`. For more information, see [Platform Invoke Examples](assetId:///15926806-f0b7-487e-93a6-4e9367ec689f).  
  
## See Also  
 [Memory Allocation](../vs140/Memory-Allocation.md)   
 [calloc](../vs140/calloc.md)   
 [free](../vs140/free.md)   
 [malloc](../vs140/malloc.md)