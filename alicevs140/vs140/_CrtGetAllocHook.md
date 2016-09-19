---
title: "_CrtGetAllocHook"
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
  - _CrtGetAllocHook
apilocation: 
  - msvcr90.dll
  - msvcrt.dll
  - msvcr100.dll
  - msvcr110_clr0400.dll
  - msvcr80.dll
  - msvcr110.dll
  - msvcr120.dll
apitype: DLLExport
ms.assetid: 036acf7c-547a-4b3f-a636-80451070d7ed
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _CrtGetAllocHook
Retrieves the current client-defined allocation function for hooking into the C run-time debug memory allocation process (debug version only).  
  
## Syntax  
  
```  
_CRT_ALLOC_HOOK _CrtGetAllocHook( void );  
```  
  
## Return Value  
 Returns the currently defined allocation hook function.  
  
## Remarks  
 `_CrtGetAllocHook` retrieves the current client-defined application hook function for the C run-time debug library memory allocation process.  
  
 For more information about using other hook-capable run-time functions and writing your own client-defined hook functions, see [Debug Hook Function Writing](../vs140/Debug-Hook-Function-Writing.md).  
  
## Requirements  
  
|Routine|Required header|  
|-------------|---------------------|  
|`_CrtGetAllocHook`|<crtdbg.h>|  
  
 For more compatibility information, see [Compatibility](../vs140/Compatibility.md) in the Introduction.  
  
## Libraries  
 Debug versions of [C run-time libraries](../vs140/CRT-Library-Features.md) only.  
  
## .NET Framework Equivalent  
 Not applicable. To call the standard C function, use `PInvoke`. For more information, see [Platform Invoke Examples](assetId:///15926806-f0b7-487e-93a6-4e9367ec689f).  
  
## See Also  
 [Debug Routines](../vs140/Debug-Routines.md)   
 [_CrtSetAllocHook](../vs140/_CrtSetAllocHook.md)