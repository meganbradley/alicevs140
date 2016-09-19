---
title: "Using Run-Time Checks Without the C Run-Time Library"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - FSharp
  - VB
  - CSharp
  - C++
  - JScript
  - VB
  - CSharp
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-debug
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 30ed90f3-9323-4784-80a4-937449eb54f6
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Using Run-Time Checks Without the C Run-Time Library
If you link your program without the C run-time library, using **/NODEFAULTLIB**, and want to use run-time checks, you must link with RunTmChk.lib.  
  
 `_RTC_Initialize` initializes your program for run-time checks. If you do not link with the C run-time library, you must check to see whether your program is compiled with run-time error checks before calling `_RTC_Initialize`, as follows:  
  
```  
#ifdef __MSVC_RUNTIME_CHECKS  
    _RTC_Initialize();  
#endif  
```  
  
 If you do not link with the C run-time library, you must also define a function called `_CRT_RTC_INITW`. `_CRT_RTC_INITW` installs your user-defined function as the default error reporting function, as follows:  
  
```  
// C version:  
_RTC_error_fnW __cdecl _CRT_RTC_INITW(  
        void *res0, void **res1, int res2, int res3, int res4)  
{  
    // set the error handler.  
    return &MyErrorFunc;   
}  
  
// C++ version:  
extern "C" _RTC_error_fnW __cdecl _CRT_RTC_INITW(  
       void *res0, void **res1, int res2, int res3, int res4)  
{  
    // set the error handler:  
    return &MyErrorFunc;  
}  
```  
  
 After you have installed the default error reporting function, you can install additional error reporting functions with `_RTC_SetErrorFuncW`. For more information, see [_RTC_SetErrorFuncW](../vs140/_RTC_SetErrorFuncW.md).  
  
## See Also  
 [Run-Time Error Checks](../vs140/How-to--Use-Native-Run-Time-Checks.md)