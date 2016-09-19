---
title: "_CrtMemDumpStatistics"
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
  - _CrtMemDumpStatistics
apilocation: 
  - msvcrt.dll
  - msvcr90.dll
  - msvcr80.dll
  - msvcr120.dll
  - msvcr110_clr0400.dll
  - msvcr110.dll
  - msvcr100.dll
apitype: DLLExport
ms.assetid: 27b9d731-3184-4a2d-b9a7-6566ab28a9fe
caps.latest.revision: 17
translation.priority.mt: 
  - de-de
  - ja-jp
---
# _CrtMemDumpStatistics
Dumps the debug header information for a specified heap state in a user-readable form (debug version only).  
  
## Syntax  
  
```  
void _CrtMemDumpStatistics(   
   const _CrtMemState *state   
);  
```  
  
#### Parameters  
 `state`  
 Pointer to the heap state to dump.  
  
## Remarks  
 The `_CrtMemDumpStatistics` function dumps the debug header information for a specified state of the heap in a user-readable form. The dump statistics can be used by the application to track allocations and detect memory problems. The memory state can contain a specific heap state or the difference between two states. When [_DEBUG](../vs140/_DEBUG.md) is not defined, calls to `_CrtMemDumpStatistics` are removed during preprocessing.  
  
 The `state` parameter must be a pointer to a `_CrtMemState` structure that has been filled in by [_CrtMemCheckpoint](../vs140/_CrtMemCheckpoint.md) or returned by [_CrtMemDifference](../vs140/_CrtMemDifference.md) before `_CrtMemDumpStatistics` is called. If `state` is `NULL`, the invalid parameter handler is invoked, as described in [Parameter Validation](../vs140/Parameter-Validation.md). If execution is allowed to continue, `errno` is set to `EINVAL` and no action is taken. For more information, see [errno, _doserrno, _sys_errlist, and _sys_nerr](../vs140/errno--_doserrno--_sys_errlist--and-_sys_nerr.md).  
  
 For more information about heap state functions and the `_CrtMemState` structure, see [Heap State Reporting Functions](../vs140/CRT-Debug-Heap-Details.md#BKMK_Heap_State_Reporting_Functions). For more information about how memory blocks are allocated, initialized, and managed in the debug version of the base heap, see [CRT Debug Heap Details](../vs140/CRT-Debug-Heap-Details.md).  
  
## Requirements  
  
|Routine|Required header|Optional headers|  
|-------------|---------------------|----------------------|  
|`_CrtMemDumpStatistics`|<crtdbg.h>|<errno.h>|  
  
 For more compatibility information, see [Compatibility](../vs140/Compatibility.md) in the Introduction.  
  
 **Libraries:** Debug versions of [CRT Library Features](../vs140/CRT-Library-Features.md) only.  
  
## .NET Framework Equivalent  
 <xref:System.Diagnostics.PerformanceCounter?qualifyHint=True>  
  
## See Also  
 [Debug Routines](../vs140/Debug-Routines.md)