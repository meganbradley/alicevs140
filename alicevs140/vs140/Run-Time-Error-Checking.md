---
title: "Run-Time Error Checking"
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
ms.assetid: c965dd01-57ad-4a3c-b1d6-5aa04f920501
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Run-Time Error Checking
The C run-time library contains the functions that support run-time error checks (RTC). Run-time error checking allows you to build your program such that certain kinds of run-time errors are reported. You specify how the errors are reported and which kinds of errors are reported. For more information, see [Run-Time Error Checks](../vs140/How-to--Use-Native-Run-Time-Checks.md).  
  
 Use the following functions to customize the way your program does run-time error checking.  
  
### Run-Time Error Checking Functions  
  
|Function|Use|.NET Framework equivalent|  
|--------------|---------|-------------------------------|  
|[_RTC_GetErrDesc](../vs140/_RTC_GetErrDesc.md)|Returns a brief description of a run-time error check type.||  
|[_RTC_NumErrors](../vs140/_RTC_NumErrors.md)|Returns the total number of errors that can be detected by run-time error checks.||  
|[_RTC_SetErrorFunc](../vs140/_RTC_SetErrorFunc.md)|Designates a function as the handler for reporting run-time error checks.||  
|[_RTC_SetErrorType](../vs140/_RTC_SetErrorType.md)|Associates an error that is detected by run-time error checks with a type.||  
  
## See Also  
 [Run-Time Routines by Category](../vs140/Run-Time-Routines-by-Category.md)   
 [/RTC (Run-Time Error Checks)](../Topic/-RTC%20\(Run-Time%20Error%20Checks\).md)   
 [runtime_checks](../vs140/runtime_checks.md)   
 [RTC sample](assetId:///b3415b09-f6fd-43dc-8c02-9a910bc2574e)   
 [Debug Routines](../vs140/Debug-Routines.md)