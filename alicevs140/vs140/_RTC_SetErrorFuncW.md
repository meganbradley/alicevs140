---
title: "_RTC_SetErrorFuncW"
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
  - _RTC_SetErrorFuncW
apilocation: 
  - msvcr110_clr0400.dll
  - msvcr110.dll
  - msvcr80.dll
  - msvcr100.dll
  - msvcr90.dll
  - msvcrt.dll
  - msvcr120.dll
apitype: DLLExport
ms.assetid: b3e0d71f-1bd3-4c37-9ede-2f638eb3c81a
caps.latest.revision: 17
translation.priority.mt: 
  - de-de
  - ja-jp
---
# _RTC_SetErrorFuncW
Designates a function as the handler for the reporting of run-time error checks (RTCs).  
  
## Syntax  
  
```  
  
      _RTC_error_fnW _RTC_SetErrorFuncW(  
   _RTC_error_fnW function   
);  
```  
  
#### Parameters  
 `function`  
 The address of the function that will handle run-time error checks.  
  
## Return Value  
 The previously defined error function; or `NULL` if there is no previously defined function.  
  
## Remarks  
 In new code, use only `_RTC_SetErrorFuncW`. `_RTC_SetErrorFunc` is only included in the library for backward compatibility.  
  
 The `_RTC_SetErrorFuncW` callback applies only to the component that it was linked in, but not globally.  
  
 Make sure that the address that you pass to `_RTC_SetErrorFuncW` is that of a valid error handling function.  
  
 If an error has been assigned a type of –1 by using [_RTC_SetErrorType](../vs140/_RTC_SetErrorType.md), the error handling function is not called.  
  
 Before you can call this function, you must first call one of the run-time error-check initialization functions. For more information, see [Using Run-Time Checks Without the C Run-Time Library](../vs140/Using-Run-Time-Checks-Without-the-C-Run-Time-Library.md).  
  
 **_RTC_error_fnW** is defined as follows:  
  
 **typedef int (__cdecl \*_RTC_error_fnW)(int**  `errorType` **, const wchar_t \*** *filename* **, int**  *linenumber* **, const wchar_t \*** `moduleName` **, const wchar_t \*** *format* **, ...);**  
  
 where:  
  
 `errorType`  
 The type of error that's specified by [_RTC_SetErrorType](../vs140/_RTC_SetErrorType.md).  
  
 *filename*  
 The source file where the failure occurred, or null if no debug information is available.  
  
 *linenumber*  
 The line in *filename* where the failure occurred, or 0 if no debug information is available.  
  
 `moduleName`  
 The DLL or executable name where the failure occurred.  
  
 *format*  
 printf style string to display an error message, using the remaining parameters. The first argument of the VA_ARGLIST is the RTC Error number that occurred.  
  
 For an example that shows how to use **_RTC_error_fnW**, see [Native Run-Time Checks Customization](../vs140/Native-Run-Time-Checks-Customization.md).  
  
## Requirements  
  
|Routine|Required header|  
|-------------|---------------------|  
|`_RTC_SetErrorFuncW`|<rtcapi.h>|  
  
 For more information, see [Compatibility](../vs140/Compatibility.md).  
  
## Libraries  
 All versions of the [C run-time libraries](../vs140/CRT-Library-Features.md).  
  
## .NET Framework Equivalent  
 Not applicable. To call the standard C function, use `PInvoke`. For more information, see [Platform Invoke Examples](assetId:///15926806-f0b7-487e-93a6-4e9367ec689f).  
  
## See Also  
 [_CrtDbgReport, _CrtDbgReportW](../vs140/_CrtDbgReport--_CrtDbgReportW.md)   
 [Run-Time Error Checking](../vs140/Run-Time-Error-Checking.md)