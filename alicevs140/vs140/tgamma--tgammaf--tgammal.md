---
title: "tgamma, tgammaf, tgammal"
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
  - tgamma
  - tgammaf
  - tgammal
apilocation: 
  - msvcrt.dll
  - msvcr80.dll
  - msvcr90.dll
  - msvcr100.dll
  - msvcr110.dll
  - msvcr110_clr400.dll
  - msvcr120.dll
  - api-ms-win-crt-math-l1-1-0.dll
apitype: DLLExport
ms.assetid: f1bd2681-8af2-48a9-919d-5358fd068acd
caps.latest.revision: 13
translation.priority.mt: 
  - de-de
  - ja-jp
---
# tgamma, tgammaf, tgammal
Determines the gamma function of the specified value.  
  
## Syntax  
  
```  
double tgamma(  
   double x  
);  
  
float tgamma(  
   float x  
); //C++ only  
  
long double tgamma(  
   long double x  
); //C++ only  
  
float tgammaf(  
   float x  
);  
  
long double tgammal(  
   long double x  
);  
  
```  
  
#### Parameters  
 [in] `x`  
 The value to find the gamma of.  
  
## Return Value  
 If successful, returns the gamma of `x`.  
  
 A range error may occur if the magnitude of `x` is too large or too small for the data type. A domain error or range error     may occur if `x` <=0.  
  
|Issue|Return|  
|-----------|------------|  
|x = ±0|±INFINITY|  
|x = negative integer|NaN|  
|x =  -INFINITY|NaN|  
|x = +INFINITY|+INFINITY|  
|x = NaN|NaN|  
|domain error|NaN|  
|pole error|±HUGE_VAL, ±HUGE_VALF, or ±HUGE_VALL|  
|overflow range error|±HUGE_VAL, ±HUGE_VALF, or ±HUGE_VALL|  
|underflow range error|the correct value, after rounding.|  
  
 Errors are reported as specified in [_matherr](../vs140/_matherr.md).  
  
## Remarks  
 Because C++ allows overloading, you can call overloads of tgamma that take and return float and long double types. In a C program, tgamma always takes and returns a double.  
  
 If x is a natural number, this function returns the factorial of (x-1).  
  
## Requirements  
  
|Function|C header|C++ header|  
|--------------|--------------|------------------|  
|`tgamma`,                `tgammaf`,  `tgammal`|<math.h>|<cmath\>|  
  
 For additional compatibility information, see [Compatibility](../vs140/Compatibility.md).  
  
## See Also  
 [Alphabetical Function Reference](../vs140/CRT-Alphabetical-Function-Reference.md)   
 [lgamma, lgammaf, lgammal](../vs140/lgamma--lgammaf--lgammal.md)