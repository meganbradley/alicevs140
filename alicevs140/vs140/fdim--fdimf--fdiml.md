---
title: "fdim, fdimf, fdiml"
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
  - fdim
  - fdimf
  - fdiml
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
ms.assetid: 2d4ac639-51e9-462d-84ab-fb03b06971a0
caps.latest.revision: 13
translation.priority.mt: 
  - de-de
  - ja-jp
---
# fdim, fdimf, fdiml
Determines the positive difference between the first and second values.  
  
## Syntax  
  
```  
double fdim(  
   double x,   
   double y  
);  
  
float fdim(  
   float x,   
   float y  
); //C++ only  
  
long double fdim(  
   long double x,   
   long double y  
); //C++ only  
  
float fdimf(  
   float x,   
   float y  
);  
  
long double fdiml(  
   long double x,   
   long double y  
);  
  
```  
  
#### Parameters  
 [in] `x`  
 The first value.  
  
 [in] `y`  
 The second value.  
  
## Return Value  
 Returns the positive difference between `x` and `y`:  
  
|Return value|Scenario|  
|------------------|--------------|  
|x-y|if x > y|  
|0|if x <= y|  
  
 Otherwise, may return one of the following errors:  
  
|Issue|Return|  
|-----------|------------|  
|Overflow range error|+HUGE_VAL, +HUGE_VALF, or +HUGE_VALL|  
|Underflow range error|correct value (after rounding)|  
|`x` or `y` is NaN|NaN|  
  
 Errors are reported as specified in [_matherr](../vs140/_matherr.md).  
  
## Remarks  
 Because C++ allows overloading, you can call overloads of `fdim` that take and return float and long double types. In a C program, `fdim` always takes and returns a double.  
  
 Except for the NaN handling, this function is equivalent to [fmax](../vs140/fmax--fmaxf--fmaxl.md)(`x`-`y,` 0).  
  
## Requirements  
  
|Function|C header|C++ header|  
|--------------|--------------|------------------|  
|`fdim`,                `fdimf`,  `fdiml`|<math.h>|<cmath\>|  
  
 For additional compatibility information, see [Compatibility](../vs140/Compatibility.md).  
  
## See Also  
 [Alphabetical Function Reference](../vs140/CRT-Alphabetical-Function-Reference.md)   
 [fmax, fmaxf, fmaxl](../vs140/fmax--fmaxf--fmaxl.md)   
 [abs](../vs140/abs--labs--llabs--_abs64.md)