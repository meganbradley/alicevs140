---
title: "atan, atanf, atanl, atan2, atan2f, atan2l"
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
  - atan2f
  - atan2l
  - atan2
  - atanf
  - atan
  - atanl
apilocation: 
  - msvcrt.dll
  - msvcr110.dll
  - msvcr110_clr0400.dll
  - msvcr120.dll
  - msvcr90.dll
  - msvcr80.dll
  - msvcr100.dll
apitype: DLLExport
ms.assetid: 7a87a18e-c94d-4727-9cb1-1bb5c2725ae4
caps.latest.revision: 21
translation.priority.ht: 
  - de-de
  - ja-jp
---
# atan, atanf, atanl, atan2, atan2f, atan2l
Calculates the arctangent of `x` (`atan`, `atanf`, and `atanl`) or the arctangent of `y`/`x` (`atan2`, `atan2f`, and `atan2l`).  
  
## Syntax  
  
```  
double atan(   
   double x   
);  
float atan(  
   float x   
);  // C++ only  
long double atan(  
   long double x  
);  // C++ only  
double atan2(   
   double y,   
   double x   
);  
float atan2(  
   float y,  
   float x  
);  // C++ only  
long double atan2(  
   long double y,  
   long double x  
);  // C++ only  
float atanf(   
   float x   
);  
long double atanl(  
   long double x  
);  
float atan2f(  
   float y,  
   float x  
);  
long double atan2l(  
   long double y,  
   long double x  
);  
```  
  
#### Parameters  
 `x`, `y`  
 Any numbers.  
  
## Return Value  
 `atan` returns the arctangent of `x` in the range –π/2 to π/2 radians. `atan2` returns the arctangent of `y/x` in the range –π to π radians. If `x` is 0, `atan` returns 0. If both parameters of `atan2` are 0, the function returns 0. All results are in radians.  
  
 `atan2` uses the signs of both parameters to determine the quadrant of the return value.  
  
|Input|SEH Exception|Matherr Exception|  
|-----------|-------------------|-----------------------|  
|± `QNAN`,`IND`|none|`_DOMAIN`|  
  
## Remarks  
 The `atan` function calculates the arctangent (the inverse tangent function) of `x`. `atan2` calculates the arctangent of `y`/`x` (if `x` equals 0, `atan2` returns π/2 if `y` is positive, -π/2 if `y` is negative, or 0 if `y` is 0.)  
  
 `atan` has an implementation that uses Streaming SIMD Extensions 2 (SSE2). For information and restrictions about using the SSE2 implementation, see [_set_SSE2_enable](../vs140/_set_SSE2_enable.md).  
  
 Because C++ allows overloading, you can call overloads of `atan` and `atan2`. In a C program, `atan` and `atan2` always take and return doubles.  
  
## Requirements  
  
|Routine|Required header|  
|-------------|---------------------|  
|`atan`, `atan2`, `atanf`, `atan2f`, `atanl`, `atan2l`|<math.h>|  
  
## Example  
  
```  
// crt_atan.c  
// arguments: 5 0.5  
#include <math.h>  
#include <stdio.h>  
#include <errno.h>  
  
int main( int ac, char* av[] )   
{  
   double x, y, theta;  
   if( ac != 3 ){  
      fprintf( stderr, "Usage: %s <x> <y>\n", av[0] );  
      return 1;  
   }  
   x = atof( av[1] );  
   theta = atan( x );  
   printf( "Arctangent of %f: %f\n", x, theta );  
   y = atof( av[2] );  
   theta = atan2( y, x );  
   printf( "Arctangent of %f / %f: %f\n", y, x, theta );   
   return 0;  
}  
```  
  
 **Arctangent of 5.000000: 1.373401**  
**Arctangent of 0.500000 / 5.000000: 0.099669**   
## .NET Framework Equivalent  
  
-   [System::Math::Atan](https://msdn.microsoft.com/en-us/library/system.math.atan.aspx)  
  
-   [System::Math::Atan2](https://msdn.microsoft.com/en-us/library/system.math.atan2.aspx)  
  
## See Also  
 [Floating-Point Support](../vs140/Floating-Point-Support.md)   
 [acos, acosf, acosl](../vs140/acos--acosf--acosl.md)   
 [asin, asinf, asinl](../vs140/asin--asinf--asinl.md)   
 [cos, cosf, cosl, cosh, coshf, coshl](../vs140/cos--cosf--cosl--cosh--coshf--coshl.md)   
 [_matherr](../vs140/_matherr.md)   
 [sin, sinf, sinl, sinh, sinhf, sinhl](../vs140/sin--sinf--sinl--sinh--sinhf--sinhl.md)   
 [tan, tanf, tanl, tanh, tanhf, tanhl](../vs140/tan--tanf--tanl--tanh--tanhf--tanhl.md)   
 [_CIatan](../vs140/_CIatan.md)   
 [CIatan2](../vs140/_CIatan2.md)