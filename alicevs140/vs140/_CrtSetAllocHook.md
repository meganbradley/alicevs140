---
title: "_CrtSetAllocHook"
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
  - _CrtSetAllocHook
apilocation: 
  - msvcr110_clr0400.dll
  - msvcr110.dll
  - msvcr100.dll
  - msvcr120.dll
  - msvcr90.dll
  - msvcrt.dll
  - msvcr80.dll
apitype: DLLExport
ms.assetid: 405df37b-2fd1-42c8-83bc-90887f17f29d
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _CrtSetAllocHook
Installs a client-defined allocation function by hooking it into the C run-time debug memory allocation process (debug version only).  
  
## Syntax  
  
```  
_CRT_ALLOC_HOOK _CrtSetAllocHook(  
   _CRT_ALLOC_HOOK allocHook   
);  
```  
  
#### Parameters  
 `allocHook`  
 New client-defined allocation function to hook into the C run-time debug memory allocation process.  
  
## Return Value  
 Returns the previously defined allocation hook function, or `NULL` if `allocHook` is `NULL`.  
  
## Remarks  
 `_CrtSetAllocHook` allows an application to hook its own allocation function into the C run-time debug library memory allocation process. As a result, every call to a debug allocation function to allocate, reallocate, or free a memory block triggers a call to the application's hook function. `_CrtSetAllocHook` provides an application with an easy method for testing how the application handles insufficient memory situations, the ability to examine allocation patterns, and the opportunity to log allocation information for later analysis. When [_DEBUG](../vs140/_DEBUG.md) is not defined, calls to `_CrtSetAllocHook` are removed during preprocessing.  
  
 The `_CrtSetAllocHook` function installs the new client-defined allocation function specified in `allocHook` and returns the previously defined hook function. The following example demonstrates how a client-defined allocation hook should be prototyped:  
  
```  
int YourAllocHook( int allocType, void *userData, size_t size, int   
blockType, long requestNumber, const unsigned char *filename, int   
lineNumber);  
```  
  
 The `allocType` argument specifies the type of allocation operation `(_HOOK_ALLOC`, `_HOOK_REALLOC`, and `_HOOK_FREE`) that triggered the call to the allocation's hook function. When the triggering allocation type is `_HOOK_FREE`, `userData` is a pointer to the user data section of the memory block about to be freed. However, when the triggering allocation type is `_HOOK_ALLOC` or `_HOOK_REALLOC`, `userData` is `NULL` because the memory block has not been allocated yet.  
  
 `size` specifies the size of the memory block in bytes, `blockType` indicates the type of the memory block, `requestNumber` is the object allocation order number of the memory block, and, if available, `filename` and `lineNumber` specify the source file name and line number where the triggering allocation operation was initiated.  
  
 After the hook function has finished processing, it must return a Boolean value, which tells the main C run-time allocation process how to continue. When the hook function wants the main allocation process to continue as if the hook function had never been called, then the hook function should return `TRUE`. This causes the original triggering allocation operation to be executed. Using this implementation, the hook function can gather and save allocation information for later analysis, without interfering with the current allocation operation or state of the debug heap.  
  
 When the hook function wants the main allocation process to continue as if the triggering allocation operation was called and it failed, then the hook function should return `FALSE`. Using this implementation, the hook function can simulate a wide range of memory conditions and debug heap states to test how the application handles each situation.  
  
 To clear the hook function, pass `NULL` to `_CrtSetAllocHook`.  
  
 For more information about how `_CrtSetAllocHook` can be used with other memory management functions or how to write your own client-defined hook functions, see [Debug Hook Function Writing](../vs140/Debug-Hook-Function-Writing.md).  
  
> [!NOTE]
>  `_CrtSetAllocHook` is not supported under `/clr:pure`.  
  
## Requirements  
  
|Routine|Required header|  
|-------------|---------------------|  
|`_CrtSetAllocHook`|<crtdbg.h>|  
  
 For more compatibility information, see [Compatibility](../vs140/Compatibility.md) in the Introduction.  
  
## Libraries  
 Debug versions of [C run-time libraries](../vs140/CRT-Library-Features.md) only.  
  
## Example  
 For a sample of how to use `_CrtSetAllocHook`, see [crt_dbg2](assetId:///21e1346a-6a17-4f57-b275-c76813089167).  
  
## .NET Framework Equivalent  
 Not applicable. To call the standard C function, use `PInvoke`. For more information, see [Platform Invoke Examples](assetId:///15926806-f0b7-487e-93a6-4e9367ec689f).  
  
## See Also  
 [Debug Routines](../vs140/Debug-Routines.md)   
 [_CrtGetAllocHook](../vs140/_CrtGetAllocHook.md)