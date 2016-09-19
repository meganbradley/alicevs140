---
title: "_RPT, _RPTF, _RPTW, _RPTFW Macros"
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
apilocation: 
  - msvcr90.dll
  - msvcr100.dll
  - msvcr110.dll
  - msvcr110_clr0400.dll
  - msvcr80.dll
  - msvcr120.dll
apitype: DLLExport
ms.assetid: a5bf8b30-57f7-4971-8030-e773b7a1ae13
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _RPT, _RPTF, _RPTW, _RPTFW Macros
Tracks an application's progress by generating a debug report (debug version only). Note that *n* specifies the number of arguments in `args` and can be 0, 1, 2, 3, 4, or 5.  
  
## Syntax  
  
```  
  
      _RPT  
      n  
      (  
   reportType,  
   format,  
...[args]  
);  
_RPTFn(  
   reportType,  
   format,  
   [args]  
);  
_RPTWn(  
   reportType,  
   format   
   [args]  
);  
_RPTFWn(  
   reportType,  
   format   
   [args]  
);  
```  
  
#### Parameters  
 `reportType`  
 Report type: `_CRT_WARN`, `_CRT_ERROR`, or `_CRT_ASSERT`.  
  
 `format`  
 Format-control string used to create the user message.  
  
 `args`  
 Substitution arguments used by `format`.  
  
## Remarks  
 All these macros take the `reportType`and `format`parameters. In addition, they might also take up to four additional arguments, signified by the number appended to the macro name. For example, `_RPT0` and `_RPTF0` take no additional arguments, `_RPT1` and `_RPTF1` take `arg1`, `_RPT2` and `_RPTF2` take `arg1` and `arg2`, and so on.  
  
 The `_RPT` and `_RPTF` macros are similar to the [printf](../vs140/printf--_printf_l--wprintf--_wprintf_l.md) function, because they can be used to track an application's progress during the debugging process. However, these macros are more flexible than `printf` because they do not need to be enclosed in `#ifdef` statements to prevent them from being called in a retail build of an application. This flexibility is achieved by using the [_DEBUG](../vs140/_DEBUG.md) macro; the `_RPT` and `_RPTF` macros are only available when the `_DEBUG` flag is defined. When `_DEBUG` is not defined, calls to these macros are removed during preprocessing.  
  
 The `_RPTW` and `_RPTFW` macros are wide-character versions of these macros. They are like `wprintf` and take wide-character strings as arguments.  
  
 The `_RPT` macros call the [_CrtDbgReport](../vs140/_CrtDbgReport--_CrtDbgReportW.md) function to generate a debug report with a user message. The `_RPTW` macros call the `_CrtDbgReportW` function to generate the same report with wide characters. The `_RPTF` and `_RPTFW` macros create a debug report with the source file and line number where the report macro was called, in addition to the user message. The user message is created by substituting the `arg`[*n*] arguments into the `format` string, using the same rules defined by the [printf](../vs140/printf--_printf_l--wprintf--_wprintf_l.md) function.  
  
 `_CrtDbgReport` or `_CrtDbgReportW` generates the debug report and determines its destinations based on the current report modes and file defined for `reportType`. The [_CrtSetReportMode](../vs140/_CrtSetReportMode.md) and [_CrtSetReportFile](../vs140/_CrtSetReportFile.md) functions are used to define the destinations for each report type.  
  
 If an `_RPT` macro is called and neither `_CrtSetReportMode` nor `_CrtSetReportFile` has been called, messages are displayed as follows.  
  
|Report type|Output destination|  
|-----------------|------------------------|  
|`_CRT_WARN`|Warning text is not displayed.|  
|`_CRT_ERROR`|A pop-up window. Same as if `_CrtSetReportMode(_CRT_ERROR, _CRTDBG_MODE_WNDW);` had been specified.|  
|`_CRT_ASSERT`|Same as `_CRT_ERROR`.|  
  
 When the destination is a debug message window and the user chooses the **Retry** button, `_CrtDbgReport` or `_CrtDbgReportW` returns 1, causing these macros to start the debugger, provided that just-in-time (JIT) debugging is enabled. For more information about using these macros as a debugging error handling mechanism, see [Using Macros for Verification and Reporting](../vs140/Macros-for-Reporting.md).  
  
 Two other macros exist that generate a debug report. The [_ASSERT](../vs140/_ASSERT--_ASSERTE--_ASSERT_EXPR-Macros.md) macro generates a report, but only when its expression argument evaluates to FALSE. [_ASSERTE](../vs140/_ASSERT--_ASSERTE--_ASSERT_EXPR-Macros.md) is exactly like `_ASSERT`, but includes the failed expression in the generated report.  
  
## Requirements  
  
|Macro|Required header|  
|-----------|---------------------|  
|`_RPT` macros|<crtdbg.h>|  
|`_RPTF` macros|<crtdbg.h>|  
|`_RPTW` macros|<crtdbg.h>|  
|`_RPTFW` macros|<crtdbg.h>|  
  
 For more compatibility information, see [Compatibility](../vs140/Compatibility.md) in the Introduction.  
  
## Libraries  
 Debug versions of [C run-time libraries](../vs140/CRT-Library-Features.md) only.  
  
 Although these are macros and are obtained by including Crtdbg.h, the application must link with one of the debug libraries because these macros call other run-time functions.  
  
## Example  
 See the example in the [_ASSERT](../vs140/_ASSERT--_ASSERTE--_ASSERT_EXPR-Macros.md) topic.  
  
## .NET Framework Equivalent  
 Not applicable. To call the standard C function, use `PInvoke`. For more information, see [Platform Invoke Examples](assetId:///15926806-f0b7-487e-93a6-4e9367ec689f).  
  
## See Also  
 [Debug Routines](../vs140/Debug-Routines.md)