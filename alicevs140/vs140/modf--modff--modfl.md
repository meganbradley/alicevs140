---
title: "modf, modff, modfl"
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
  - modff
  - modf
  - modfl
apilocation: 
  - msvcr100.dll
  - msvcr110_clr0400.dll
  - msvcr120.dll
  - msvcr80.dll
  - msvcrt.dll
  - msvcr90.dll
  - msvcr110.dll
  - api-ms-win-crt-math-l1-1-0.dll
apitype: DLLExport
ms.assetid: b1c7abf5-d476-43ca-a03c-02072a86e32d
caps.latest.revision: 13
translation.priority.mt: 
  - de-de
  - ja-jp
---
# modf, modff, modfl
Splits a floating-point value into fractional and integer parts.  
  
## Syntax  
  
```  
double modf(  
   double x,  
   double * intptr   
);  
float modf(  
   float x,  
   float * intptr  
);  // C++ only  
long double modf(  
   long double x,  
   long double * intptr  
);  // C++ only  
float modff(  
   float x,  
   float * intptr   
);  
long double modfl(  
   long double x,  
   long double * intptr  
);  
```  
  
#### Parameters  
 *x*  
 Floating-point value.  
  
 `intptr`  
 Pointer to stored integer portion.  
  
## Return Value  
 This function returns the signed fractional portion of *x*. There is no error return.  
  
## Remarks  
 The `modf` functions break down the floating-point value `x` into fractional and integer parts, each of which has the same sign as `x`. The signed fractional portion of `x` is returned. The integer portion is stored as a floating-point value at `intptr.`  
  
 `modf` has an implementation that uses Streaming SIMD Extensions 2 (SSE2). See [_set_SSE2_enable](../vs140/_set_SSE2_enable.md) for information and restrictions on using the SSE2 implementation.  
  
 C++ allows overloading, so you can call overloads of `modf` that take and return `float` or `long double` parameters. In a C program, `modf` always takes two double values and returns a double value.  
  
## Requirements  
  
|Routine|Required header|  
|-------------|---------------------|  
|`modf`, `modff`, `modfl`|C: <math.h><br /><br /> C++: , <cmath\> or <math.h>|  
  
 For additional compatibility information, see [Compatibility](../vs140/Compatibility.md) in the Introduction.  
  
## Libraries  
 All versions of the [C run-time libraries](../vs140/CRT-Library-Features.md).  
  
## Example  
  
```  
// crt_modf.c  
  
#include <math.h>  
#include <stdio.h>  
  
int main( void )  
{  
   double x, y, n;  
  
   x = -14.87654321;      /* Divide x into its fractional */  
   y = modf( x, &n );     /* and integer parts            */  
  
   printf( "For %f, the fraction is %f and the integer is %.f\n",   
           x, y, n );  
}  
```  
  
## Output  
  
```  
For -14.876543, the fraction is -0.876543 and the integer is -14  
```  
  
## See Also  
 [Floating-Point Support](../vs140/Floating-Point-Support.md)   
 [frexp](../vs140/frexp.md)   
 [ldexp](../vs140/ldexp.md)