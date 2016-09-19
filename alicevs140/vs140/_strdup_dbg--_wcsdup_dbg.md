---
title: "_strdup_dbg, _wcsdup_dbg"
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
  - _strdup_dbg
  - _wcsdup_dbg
apilocation: 
  - msvcr110_clr0400.dll
  - msvcr80.dll
  - msvcr110.dll
  - msvcr100.dll
  - msvcr120.dll
  - msvcrt.dll
  - msvcr90.dll
apitype: DLLExport
ms.assetid: 681db70c-d124-43ab-b83e-5eeea9035097
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _strdup_dbg, _wcsdup_dbg
Versions of [_strdup and _wcsdup](../vs140/_strdup--_wcsdup--_mbsdup.md) that use the debug version of `malloc`.  
  
## Syntax  
  
```  
char *_strdup_dbg(  
   const char *strSource,  
   int blockType,  
   const char *filename,  
   int linenumber   
);  
wchar_t *_wcsdup_dbg(  
   const wchar_t *strSource,  
   int blockType,  
   const char *filename,  
   int linenumber   
);  
```  
  
#### Parameters  
 `strSource`  
 Null-terminated source string.  
  
 `blockType`  
 Requested type of memory block: `_CLIENT_BLOCK` or `_NORMAL_BLOCK`.  
  
 `filename`  
 Pointer to name of source file that requested allocation operation or NULL.  
  
 `linenumber`  
 Line number in source file where allocation operation was requested or NULL.  
  
## Return Value  
 Each of these functions returns a pointer to the storage location for the copied string or `NULL` if storage cannot be allocated.  
  
## Remarks  
 The `_strdup_dbg` and `_wcsdup_dbg` functions are identical to `_strdup` and `_wcsdup` except that, when `_DEBUG` is defined, these functions use the debug version of `malloc`, `_malloc_dbg`, to allocate memory for the duplicated string. For information on the debugging features of `_malloc_dbg`, see [_malloc_dbg](../vs140/_malloc_dbg.md).  
  
 You do not need to call these functions explicitly in most cases. Instead, you can define the flag `_CRTDBG_MAP_ALLOC`. When `_CRTDBG_MAP_ALLOC` is defined, calls to `_strdup` and `_wcsdup` are remapped to `_strdup_dbg` and `_wcsdup_dbg`, respectively, with the `blockType` set to `_NORMAL_BLOCK`. Thus, you do not need to call these functions explicitly unless you want to mark the heap blocks as `_CLIENT_BLOCK`. For more information on block types, see [Types of Blocks on the Debug Heap](../vs140/CRT-Debug-Heap-Details.md#BKMK_Types_of_blocks_on_the_debug_heap).  
  
### Generic-Text Routine Mappings  
  
|TCHAR.H routine|_UNICODE & _MBCS not defined|_MBCS defined|_UNICODE defined|  
|---------------------|------------------------------------|--------------------|-----------------------|  
|`_tcsdup_dbg`|`_strdup_dbg`|`_mbsdup`|`_wcsdup_dbg`|  
  
## Requirements  
  
|Routine|Required header|  
|-------------|---------------------|  
|`_strdup_dbg`, `_wcsdup_dbg`|<crtdbg.h>|  
  
 For additional compatibility information, see [Compatibility](../vs140/Compatibility.md) in the Introduction.  
  
## Libraries  
 All debug versions of the [C run-time libraries](../vs140/CRT-Library-Features.md).  
  
## .NET Framework Equivalent  
 [System::String::Clone](https://msdn.microsoft.com/en-us/library/system.string.clone.aspx)  
  
## See Also  
 [String Manipulation](../vs140/String-Manipulation--CRT-.md)   
 [_strdup, _wcsdup, _mbsdup](../vs140/_strdup--_wcsdup--_mbsdup.md)   
 [Debug Versions of Heap Allocation Functions](../vs140/Debug-Versions-of-Heap-Allocation-Functions.md)