---
title: "_CrtGetReportHook"
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
  - _CrtGetReportHook
apilocation: 
  - msvcr100.dll
  - msvcr90.dll
  - msvcr110.dll
  - msvcr110_clr0400.dll
  - msvcr80.dll
  - msvcrt.dll
  - msvcr120.dll
apitype: DLLExport
ms.assetid: 922758ed-7edd-4359-9c92-0535192dc11a
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _CrtGetReportHook
Retrieves the client-defined reporting function for hooking it into the C run time for the debug reporting process (debug version only).  
  
## Syntax  
  
```  
_CRT_REPORT_HOOK _CrtGetReportHook( void );  
```  
  
## Return Value  
 Returns the current client-defined reporting function.  
  
## Remarks  
 `_CrtGetReportHook` allows an application to retrieve the current reporting function for the C run-time debug library reporting process.  
  
 For more information about using other hook-capable run-time functions and writing your own client-defined hook functions, see [Debug Hook Function Writing](../vs140/Debug-Hook-Function-Writing.md).  
  
## Requirements  
  
|Routine|Required header|  
|-------------|---------------------|  
|`_CrtGetReportHook`|<crtdbg.h>|  
  
 For more compatibility information, see [Compatibility](../vs140/Compatibility.md) in the Introduction.  
  
## Libraries  
 Debug versions of [C run-time libraries](../vs140/CRT-Library-Features.md) only.  
  
## Example  
 For a sample of how to use `_CrtSetReportHook`, see [report](assetId:///f6e08c30-6bd9-459a-830a-56deec0d2051).  
  
## .NET Framework Equivalent  
 Not applicable. To call the standard C function, use `PInvoke`. For more information, see [Platform Invoke Examples](assetId:///15926806-f0b7-487e-93a6-4e9367ec689f).  
  
## See Also  
 [Debug Routines](../vs140/Debug-Routines.md)   
 [_CrtSetReportHook](../vs140/_CrtSetReportHook.md)