---
title: "_RTC_GetErrDesc"
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
  - _RTC_GetErrDesc
apilocation: 
  - msvcr100.dll
  - msvcr110.dll
  - msvcr90.dll
  - msvcr120.dll
  - msvcr110_clr0400.dll
  - msvcr80.dll
  - msvcrt.dll
apitype: DLLExport
ms.assetid: 7994ec2b-5488-4fd4-806d-a166c9a9f927
caps.latest.revision: 14
translation.priority.mt: 
  - de-de
  - ja-jp
---
# _RTC_GetErrDesc
Returns a brief description of a run-time error check (RTC) type.  
  
## Syntax  
  
```  
  
      const char * _RTC_GetErrDesc(  
   _RTC_ErrorNumber errnum   
);  
```  
  
#### Parameters  
 *errnum*  
 A number between zero and one less than the value returned by `_RTC_NumErrors`.  
  
## Return Value  
 A character string that contains a short description of one of the error types detected by the run-time error check system. If error is less than zero or greater than or equal to the value returned by [_RTC_NumErrors](../vs140/_RTC_NumErrors.md), `_RTC_GetErrDesc` returns NULL.  
  
## Requirements  
  
|Routine|Required header|  
|-------------|---------------------|  
|`_RTC_GetErrDesc`|<rtcapi.h>|  
  
 For more information, see [Compatibility](../vs140/Compatibility.md).  
  
## Libraries  
 All versions of the [C run-time libraries](../vs140/CRT-Library-Features.md).  
  
## .NET Framework Equivalent  
 Not applicable. To call the standard C function, use `PInvoke`. For more information, see [Platform Invoke Examples](assetId:///15926806-f0b7-487e-93a6-4e9367ec689f).  
  
## See Also  
 [_RTC_NumErrors](../vs140/_RTC_NumErrors.md)   
 [Run-Time Error Checking](../vs140/Run-Time-Error-Checking.md)