---
title: "Native Run-Time Checks Customization"
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
ms.assetid: 76a365fe-6439-49db-8603-34058b78e5a8
caps.latest.revision: 20
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Native Run-Time Checks Customization
When you compile with **/RTC** (run-time checks) or use the `runtime_checks` pragma, the C run-time library provides native run-time checks. In some cases, you might want to customize run-time checking:  
  
-   To route run-time check messages to a file or destination other than the default.  
  
-   To specify an output destination for run-time check messages under a third-party debugger.  
  
-   To report run-time check messages from a program compiled with a release version of the C run-time library. Release versions of the library do not use `_CrtDbgReportW` to report run-time errors. Instead, they display an **Assert** dialog box for each run-time error.  
  
 To customize run-time error checking, you can:  
  
-   Write a run-time error reporting function. For more information, see [How to: Write a Run-Time Error Reporting Function](../vs140/How-to--Write-a-Run-Time-Error-Reporting-Function.md).  
  
-   Customize the error message destination.  
  
-   Query for information about run-time check errors.  
  
## Customize the Error Message Destination  
 If you use `_CrtDbgReportW` to report errors, you can use `_CrtSetReportMode` to specify the destination of error messages.  
  
 If you use a custom reporting function, use `_RTC_SetErrorType` to associate an error with a report type.  
  
## Query for Information About Run-Time Checks  
 `_RTC_NumErrors` returns the number of error types detected by run-time error checks. To get a brief description of each error, you can loop from 0 to the return value of `_RTC_NumErrors`, passing the iteration value to `_RTC_GetErrDesc` on each loop. For more information, see [_RTC_NumErrors](../vs140/_RTC_NumErrors.md) and [_RTC_GetErrDesc](../vs140/_RTC_GetErrDesc.md).  
  
## See Also  
 [How to: Use Native Run-Time Checks](../vs140/How-to--Use-Native-Run-Time-Checks.md)   
 [runtime_checks](../vs140/runtime_checks.md)   
 [_CrtDbgReportW](../vs140/_CrtDbgReport--_CrtDbgReportW.md)