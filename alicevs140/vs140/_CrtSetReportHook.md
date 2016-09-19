---
title: "_CrtSetReportHook"
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
  - _CrtSetReportHook
apilocation: 
  - msvcrt.dll
  - msvcr90.dll
  - msvcr100.dll
  - msvcr110.dll
  - msvcr80.dll
  - msvcr110_clr0400.dll
  - msvcr120.dll
apitype: DLLExport
ms.assetid: 1ae7c64f-8c84-4797-9574-b59f00f7a509
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _CrtSetReportHook
Installs a client-defined reporting function by hooking it into the C run-time debug reporting process (debug version only).  
  
## Syntax  
  
```  
_CRT_REPORT_HOOK _CrtSetReportHook(   
   _CRT_REPORT_HOOK reportHook   
);  
```  
  
#### Parameters  
 `reportHook`  
 New client-defined reporting function to hook into the C run-time debug reporting process.  
  
## Return Value  
 Returns the previous client-defined reporting function.  
  
## Remarks  
 `_CrtSetReportHook` allows an application to use its own reporting function into the C run-time debug library reporting process. As a result, whenever [_CrtDbgReport](../vs140/_CrtDbgReport--_CrtDbgReportW.md) is called to generate a debug report, the application's reporting function is called first. This functionality enables an application to perform operations such as filtering debug reports so it can focus on specific allocation types or send a report to destinations not available by using `_CrtDbgReport`. When [_DEBUG](../vs140/_DEBUG.md) is not defined, calls to `_CrtSetReportHook` are removed during preprocessing.  
  
 For a more robust version of `_CrtSetReportHook`, see [_CrtSetReportHook2](../vs140/_CrtSetReportHook2--_CrtSetReportHookW2.md).  
  
 The `_CrtSetReportHook` function installs the new client-defined reporting function specified in `reportHook` and returns the previous client-defined hook. The following example demonstrates how a client-defined report hook should be prototyped:  
  
```  
int YourReportHook( int reportType, char *message, int *returnValue );  
```  
  
 where `reportType` is the debug report type (`_CRT_WARN`, `_CRT_ERROR`, or `_CRT_ASSERT`), `message` is the fully assembled debug user message to be contained in the report, and `returnValue` is the value specified by the client-defined reporting function that should be returned by `_CrtDbgReport`. For a complete description of the available report types, see the [_CrtSetReportMode](../vs140/_CrtSetReportMode.md) function.  
  
 If the client-defined reporting function completely handles the debug message such that no further reporting is required, then the function should return `TRUE`. When the function returns `FALSE`, `_CrtDbgReport` is called to generate the debug report using the current settings for the report type, mode, and file. In addition, by specifying the `_CrtDbgReport` return value in `returnValue`, the application can also control whether a debug break occurs. For a complete description of how the debug report is configured and generated, see `_CrtSetReportMode`, [_CrtSetReportFile](../vs140/_CrtSetReportFile.md), and `_CrtDbgReport`.  
  
 For more information about using other hook-capable run-time functions and writing your own client-defined hook functions, see [Debug Hook Function Writing](../vs140/Debug-Hook-Function-Writing.md).  
  
> [!NOTE]
>  If your application is compiled with `/clr` and the reporting function is called after the application has exited main, the CLR will throw an exception if the reporting function calls any CRT functions.  
  
## Requirements  
  
|Routine|Required header|  
|-------------|---------------------|  
|`_CrtSetReportHook`|<crtdbg.h>|  
  
 For more compatibility information, see [Compatibility](../vs140/Compatibility.md) in the Introduction.  
  
## Libraries  
 Debug versions of [C run-time libraries](../vs140/CRT-Library-Features.md) only.  
  
## .NET Framework Equivalent  
 Not applicable. To call the standard C function, use `PInvoke`. For more information, see [Platform Invoke Examples](assetId:///15926806-f0b7-487e-93a6-4e9367ec689f).  
  
## See Also  
 [Debug Routines](../vs140/Debug-Routines.md)   
 [_CrtGetReportHook](../vs140/_CrtGetReportHook.md)