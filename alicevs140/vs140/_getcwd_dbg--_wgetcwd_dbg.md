---
title: "_getcwd_dbg, _wgetcwd_dbg"
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
  - _wgetcwd_dbg
  - _getcwd_dbg
apilocation: 
  - msvcr90.dll
  - msvcrt.dll
  - msvcr100.dll
  - msvcr110_clr0400.dll
  - msvcr80.dll
  - msvcr120.dll
  - msvcr110.dll
apitype: DLLExport
ms.assetid: 8d5d151f-d844-4aa6-a28c-1c11a22dc00d
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _getcwd_dbg, _wgetcwd_dbg
Debug versions of the [_getcwd, _wgetcwd](../vs140/_getcwd--_wgetcwd.md) functions (only available during debug).  
  
## Syntax  
  
```  
char *_getcwd_dbg(   
   char *buffer,  
   int maxlen,  
   int blockType,  
   const char *filename,  
   int linenumber   
);  
wchar_t *_wgetcwd_dbg(   
   wchar_t *buffer,  
   int maxlen,  
   int blockType,  
   const char *filename,  
   int linenumber   
);  
```  
  
#### Parameters  
 `buffer`  
 Storage location for the path.  
  
 `maxlen`  
 Maximum length of the path in characters: `char` for `_getcwd_dbg` and `wchar_t` for `_wgetcwd_dbg`.  
  
 `blockType`  
 Requested type of the memory block: `_CLIENT_BLOCK` or `_NORMAL_BLOCK`.  
  
 `filename`  
 Pointer to the name of the source file that requested the allocation operation or `NULL`.  
  
 `linenumber`  
 Line number in the source file where the allocation operation was requested or `NULL`.  
  
## Return Value  
 Returns a pointer to `buffer`. A `NULL` return value indicates an error, and `errno` is set either to `ENOMEM`, indicating that there is insufficient memory to allocate `maxlen` bytes (when a `NULL` argument is given as `buffer`), or to `ERANGE`, indicating that the path is longer than `maxlen` characters.  
  
 For more information, see [errno, _doserrno, _sys_errlist, and _sys_nerr](../vs140/errno--_doserrno--_sys_errlist--and-_sys_nerr.md).  
  
## Remarks  
 The `_getcwd_dbg` and `_wgetcwd_dbg` functions are identical to `_getcwd` and `_wgetcwd` except that, when _`DEBUG` is defined, these functions use the debug version of `malloc` and `_malloc_dbg` to allocate memory if `NULL` is passed as the first parameter. For more information, see [_malloc_dbg](../vs140/_malloc_dbg.md).  
  
 You do not need to call these functions explicitly in most cases. Instead, you can define the `_CRTDBG_MAP_ALLOC` flag. When `_CRTDBG_MAP_ALLOC` is defined, calls to `_getcwd`and `_wgetcwd`are remapped to `_getcwd_dbg`and `_wgetcwd_dbg`, respectively, with the `blockType` set to `_NORMAL_BLOCK`. Thus, you do not need to call these functions explicitly unless you want to mark the heap blocks as `_CLIENT_BLOCK`. For more information, see [Types of Blocks on the Debug Heap](../vs140/CRT-Debug-Heap-Details.md#BKMK_Types_of_blocks_on_the_debug_heap).  
  
## Generic-Text Routine Mappings  
  
|Tchar.h routine|_UNICODE and _MBCS not defined|_MBCS defined|_UNICODE defined|  
|---------------------|--------------------------------------|--------------------|-----------------------|  
|`_tgetcwd_dbg`|`_getcwd_dbg`|`_getcwd_dbg`|`_wgetcwd_dbg`|  
  
## Requirements  
  
|Routine|Required header|  
|-------------|---------------------|  
|`_getcwd_dbg`|<crtdbg.h>|  
|`_wgetcwd_dbg`|<crtdbg.h>|  
  
 For more compatibility information, see [Compatibility](../vs140/Compatibility.md) in the Introduction.  
  
## .NET Framework Equivalent  
 <xref:System.Environment.CurrentDirectory?qualifyHint=False>  
  
## See Also  
 [_getcwd, _wgetcwd](../vs140/_getcwd--_wgetcwd.md)   
 [Directory Control](../vs140/Directory-Control.md)   
 [Debug Versions of Heap Allocation Functions](../vs140/Debug-Versions-of-Heap-Allocation-Functions.md)