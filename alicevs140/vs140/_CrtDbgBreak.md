---
title: "_CrtDbgBreak"
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
  - _CrtDbgBreak
apilocation: 
  - msvcr90.dll
  - msvcr110.dll
  - msvcr100.dll
  - msvcr80.dll
  - msvcr110_clr0400.dll
  - msvcr120.dll
  - msvcrt.dll
apitype: DLLExport
ms.assetid: 01f8b4a2-a2c7-4e1f-9f39-e573b4a7871f
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _CrtDbgBreak
Sets a break point on a particular line of code. (Used in debug mode only.)  
  
## Syntax  
  
```  
void _CrtDbgBreak( void );  
```  
  
## Return Value  
 There is no return value.  
  
## Remarks  
 The `_CrtDbgBreak` function sets a debug breakpoint on the particular line of code where the function resides. This function is used in debug mode only and is dependent on `_DEBUG` being previously defined.  
  
 For more information about using other hook-capable run-time functions and writing your own client-defined hook functions, see [Writing Your Own Debug Hook Functions](../vs140/Debug-Hook-Function-Writing.md).  
  
## .NET Framework Equivalent  
 Not applicable. To call the standard C function, use `PInvoke`. For more information, see [Platform Invoke Examples](assetId:///15926806-f0b7-487e-93a6-4e9367ec689f).  
  
## Requirements  
  
|Routine|Required header|  
|-------------|---------------------|  
|`_CrtDbgBreak`|<CRTDBG.h>|  
  
## Libraries  
 Debug versions of [C run-time libraries](../vs140/CRT-Library-Features.md) only.  
  
## See Also  
 [Debug Routines](../vs140/Debug-Routines.md)   
 [__debugbreak](../vs140/__debugbreak.md)