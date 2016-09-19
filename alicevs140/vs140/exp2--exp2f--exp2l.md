---
title: "exp2, exp2f, exp2l"
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
  - exp2
  - exp2f
  - exp2l
apilocation: 
  - msvcrt.dll
  - msvcr80.dll
  - msvcr90.dll
  - msvcr100.dll
  - msvcr110.dll
  - msvcr110_clr0400.dll
  - api-ms-win-crt-math-l1-1-0.dll
  - msvcr110_clr400.dll
  - msvcr120.dll
apitype: DLLExport
ms.assetid: 526e3e10-201a-4610-a886-533f44ece344
caps.latest.revision: 15
translation.priority.mt: 
  - de-de
  - ja-jp
---
# exp2, exp2f, exp2l
Computes 2 raised to the specified value (ie, 2ˣ ).  
  
## Syntax  
  
```  
double exp2(  
   double x  
);  
  
float exp2(  
   float x  
);  // C++ only  
  
long double exp2(  
   long double x  
); // C++ only  
  
float exp2f(  
   float x  
);  
  
long double exp2l(  
   long double x  
);  
  
```  
  
#### Parameters  
 [in] `x`  
 The value of the exponent.  
  
## Return Value  
 If successful, returns the base-2 exponent of `x` (2ˣ) . Otherwise, may return one of the following values:  
  
|Issue|Return|  
|-----------|------------|  
|`x` = ±0|1|  
|`x` = -INFINITY|+0|  
|`x` = +INFINITY|+INFINITY|  
|`x` = NaN|NaN|  
|Overflow range error|+HUGE_VAL, +HUGE_VALF, or +HUGE_VALL|  
|Underflow range error|correct result, after rounding|  
  
 Errors are reported as specified in [_matherr](../vs140/_matherr.md).  
  
## Remarks  
 Because C++ allows overloading, you can call overloads of `exp2` that take and return float and long double types. In a C program, `exp2` always takes and returns a double.  
  
## Requirements  
  
|Routine|C header|C++ header|  
|-------------|--------------|------------------|  
|`exp`,                `expf`, `expl`|<math.h>|<cmath\>|  
  
 For additional compatibility information, see [Compatibility](../vs140/Compatibility.md).  
  
## See Also  
 [Alphabetical Function Reference](../vs140/CRT-Alphabetical-Function-Reference.md)   
 [exp](../vs140/exp--expf.md)   
 [log2](../vs140/log2--log2f--log2l.md)