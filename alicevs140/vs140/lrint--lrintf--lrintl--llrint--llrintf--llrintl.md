---
title: "lrint, lrintf, lrintl, llrint, llrintf, llrintl"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - cpp
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: article
apiname: 
  - lrint
  - lrintl
  - lrintf
  - llrint
  - llrintf
  - llrintl
apilocation: 
  - msvcrt.dll
  - msvcr80.dll
  - msvcr90.dll
  - msvcr100.dll
  - msvcr110.dll
  - msvcr110_clr400.dll
  - msvcr120.dll
  - api-ms-win-crt-math-l1-1-0.dll
  - ucrtbase.dll
apitype: DLLExport
ms.assetid: 28ccd5b3-5e6f-434f-997d-a21d51b8ce7f
caps.latest.revision: 15
translation.priority.mt: 
  - de-de
  - ja-jp
---
# lrint, lrintf, lrintl, llrint, llrintf, llrintl
Rounds the specified floating-point value to the nearest integral value, by using the current rounding mode and direction.  
  
## Syntax  
  
```  
long int lrint(  
   double x  
);  
  
long int lrint(  
   float x  
); //C++ only  
  
long int lrint(  
   long double x  
); //C++ only  
  
long int lrintf(  
   float x  
);  
  
long int lrintl(  
   long double x  
);  
  
long long int llrint(  
   double x  
);  
  
long long int llrint(  
   float x  
); //C++ only  
  
long long int llrint(  
   long double x  
); //C++ only  
  
long long int llrintf(  
   float x  
);  
  
long long int llrintl(  
   long double x  
);  
  
```  
  
#### Parameters  
 [in] `x`  
 the value to round.  
  
## Return Value  
 If successful, returns the rounded integral value of `x`.  
  
|Issue|Return|  
|-----------|------------|  
|`x` is outside the range of the return type<br /><br /> `x` = ±∞<br /><br /> `x` = NaN|Raises FE_INVALID and returns zero (0).|  
  
## Remarks  
 Because C++ allows overloading, you can call overloads of `lrint` and `llrint` that take float and long double types. In a C program, `lrint` and `llrint` always take a double.  
  
 If `x` does not represent the floating-point equivalent of an integral value, these functions raise FE_INEXACT.  
  
 **Microsoft specific**: When the result is outside the range of the return type, or when the parameter is a NaN or infinity, the return value is implementation defined. The Microsoft compiler returns a zero (0) value.  
  
## Requirements  
  
|Function|C header|C++ header|  
|--------------|--------------|------------------|  
|`lrint`,                `lrintf`, `lrintl`, `llrint`, `llrintf`, `llrintl`|<math.h>|<cmath\>|  
  
 For additional compatibility information, see [Compatibility](../vs140/Compatibility.md).  
  
## See Also  
 [Alphabetical Function Reference](../vs140/CRT-Alphabetical-Function-Reference.md)