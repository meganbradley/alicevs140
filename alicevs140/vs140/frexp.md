---
title: "frexp"
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
  - frexp
apilocation: 
  - msvcr120.dll
  - msvcr100.dll
  - msvcrt.dll
  - msvcr80.dll
  - msvcr110_clr0400.dll
  - msvcr90.dll
  - msvcr110.dll
apitype: DLLExport
ms.assetid: 9b020f2e-3967-45ec-a6a8-d467a071aa55
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# frexp
Gets the mantissa and exponent of a floating-point number.  
  
## Syntax  
  
```  
double frexp(  
   double x,  
   int *expptr   
);  
float frexp(  
   float x,  
   int * expptr  
);  // C++ only  
long double frexp(  
   long double x,  
   int * expptr  
);  // C++ only  
```  
  
#### Parameters  
 `x`  
 Floating-point value.  
  
 `expptr`  
 Pointer to stored integer exponent.  
  
## Return Value  
 `frexp` returns the mantissa. If `x` is 0, the function returns 0 for both the mantissa and the exponent. If `expptr` is `NULL`, the invalid parameter handler is invoked as described in [Parameter Validation](../vs140/Parameter-Validation.md). If execution is allowed to continue, this function sets `errno` to `EINVAL` and returns 0.  
  
## Remarks  
 The `frexp` function breaks down the floating-point value (`x`) into a mantissa (`m`) and an exponent (`n`), such that the absolute value of `m` is greater than or equal to 0.5 and less than 1.0, and `x` = `m`*2<sup>n</sup>. The integer exponent `n` is stored at the location pointed to by `expptr`.  
  
 C++ allows overloading, so you can call overloads of `frexp`. In a C program, `frexp` always takes a double and an integer and returns a double.  
  
## Requirements  
  
|Function|Required header|  
|--------------|---------------------|  
|`frexp`|<math.h>|  
  
 For additional compatibility information, see [Compatibility](../vs140/Compatibility.md) in the Introduction.  
  
## Example  
  
```  
// crt_frexp.c  
// This program calculates frexp( 16.4, &n )  
// then displays y and n.  
  
#include <math.h>  
#include <stdio.h>  
  
int main( void )  
{  
   double x, y;  
   int n;  
  
   x = 16.4;  
   y = frexp( x, &n );  
   printf( "frexp( %f, &n ) = %f, n = %d\n", x, y, n );  
}  
```  
  
 **frexp( 16.400000, &n ) = 0.512500, n = 5**   
## .NET Framework Equivalent  
 Not applicable. To call the standard C function, use `PInvoke`. For more information, see [Platform Invoke Examples](assetId:///15926806-f0b7-487e-93a6-4e9367ec689f).  
  
## See Also  
 [Floating-Point Support](../vs140/Floating-Point-Support.md)   
 [ldexp](../vs140/ldexp.md)   
 [modf, modff, modfl](../vs140/modf--modff--modfl.md)