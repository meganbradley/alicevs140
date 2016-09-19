---
title: "_CrtIsValidHeapPointer"
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
  - _CrtIsValidHeapPointer
apilocation: 
  - msvcrt.dll
  - msvcr90.dll
  - msvcr120.dll
  - msvcr110_clr0400.dll
  - msvcr100.dll
  - msvcr110.dll
  - msvcr80.dll
apitype: DLLExport
ms.assetid: caf597ce-1b05-4764-9f37-0197a982bec5
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _CrtIsValidHeapPointer
Verifies that a specified pointer is in a heap allocated by some C run-time library, but not necessarily by the caller's CRT library. In versions of the CRT before Visual Studio 2010, this verifies that the specified pointer is in the local heap (debug version only).  
  
## Syntax  
  
```  
  
      int _CrtIsValidHeapPointer(   
   const void *userData   
);  
```  
  
#### Parameters  
 `userData`  
 Pointer to the beginning of an allocated memory block.  
  
## Return Value  
 `_CrtIsValidHeapPointer` returns TRUE if the specified pointer is in the heap shared by all CRT library instances. In versions of the CRT before Visual Studio 2010, this returns TRUE if the specified pointer is in the local heap. Otherwise, the function returns FALSE.  
  
## Remarks  
 We do not recommend that you use this function. Starting with the Visual Studio 2010 CRT library, all CRT libraries share one OS heap, the *process heap*. The `_CrtIsValidHeapPointer` function reports whether the pointer was allocated in a CRT heap, but not that it was allocated by the caller's CRT library. For example, consider a block allocated by using the Visual Studio 2010 version of the CRT library. If the `_CrtIsValidHeapPointer` function exported by the Visual Studio 2012 version of the CRT library tests the pointer, it returns TRUE. This is no longer a useful test. In versions of the CRT library before Visual Studio 2010, the function is used to ensure that a specific memory address is within the local heap. The local heap refers to the heap created and managed by a particular instance of the C run-time library. If a dynamic-link library (DLL) contains a static link to the run-time library, it has its own instance of the run-time heap, and therefore its own heap, independent of the application's local heap. When [_DEBUG](../vs140/_DEBUG.md) is not defined, calls to `_CrtIsValidHeapPointer` are removed during preprocessing.  
  
 Because this function returns TRUE or FALSE, it can be passed to one of the [_ASSERT](../vs140/_ASSERT--_ASSERTE--_ASSERT_EXPR-Macros.md) macros to create a simple debugging error handling mechanism. The following example causes an assertion failure if the specified address is not located within the local heap:  
  
```  
_ASSERTE( _CrtIsValidHeapPointer( userData ) );  
```  
  
 For more information about how `_CrtIsValidHeapPointer` can be used with other debug functions and macros, see [Macros for Reporting](../vs140/Macros-for-Reporting.md). For information about how memory blocks are allocated, initialized, and managed in the debug version of the base heap, see [CRT Debug Heap Details](../vs140/CRT-Debug-Heap-Details.md).  
  
## Requirements  
  
|Routine|Required header|  
|-------------|---------------------|  
|`_CrtIsValidHeapPointer`|<crtdbg.h>|  
  
 For more compatibility information, see [Compatibility](../vs140/Compatibility.md) in the Introduction.  
  
## Libraries  
 Debug versions of [C run-time libraries](../vs140/CRT-Library-Features.md) only.  
  
## Example  
 The following example demonstrates how to test whether memory is valid when it is used with C run-time libraries before Visual Studio 2010. This example is provided for users of legacy CRT library code.  
  
```  
// crt_isvalid.c  
/*  
 * This program allocates a block of memory using _malloc_dbg  
 * and then tests the validity of this memory by calling   
 * _CrtIsMemoryBlock,_CrtIsValidPointer, and _CrtIsValidHeapPointer.  
 */  
  
#include <stdio.h>  
#include <string.h>  
#include <malloc.h>  
#include <crtdbg.h>  
  
#define  TRUE   1  
#define  FALSE  0  
  
int main( void )  
{  
        char *my_pointer;  
  
        /*   
         * Call _malloc_dbg to include the filename and line number  
         * of our allocation request in the header information  
         */  
        my_pointer = (char *)_malloc_dbg( sizeof(char) * 10,   
        _NORMAL_BLOCK, __FILE__, __LINE__ );  
  
        // Ensure that the memory got allocated correctly  
        _CrtIsMemoryBlock((const void *)my_pointer, sizeof(char) * 10,   
        NULL, NULL, NULL );  
  
         // Test for read/write accessibility  
        if (_CrtIsValidPointer((const void *)my_pointer,   
        sizeof(char) * 10, TRUE))  
                printf("my_pointer has read and write accessibility.\n");  
        else  
                printf("my_pointer only has read access.\n");  
  
        // Make sure my_pointer is within the local heap  
        if (_CrtIsValidHeapPointer((const void *)my_pointer))  
                printf("my_pointer is within the local heap.\n");  
        else  
                printf("my_pointer is not located within the local"  
                       " heap.\n");  
  
        free(my_pointer);  
}  
```  
  
## Output  
  
```  
my_pointer has read and write accessibility.  
my_pointer is within the local heap.  
```  
  
## .NET Framework Equivalent  
 Not applicable. To call the standard C function, use `PInvoke`. For more information, see [Platform Invoke Examples](assetId:///15926806-f0b7-487e-93a6-4e9367ec689f).  
  
## See Also  
 [Debug Routines](../vs140/Debug-Routines.md)