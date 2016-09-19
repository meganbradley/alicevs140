---
title: "rint, rintf, rintl"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: article
apiname: 
  - rintf
  - rintl
  - rint
apilocation: 
  - msvcr90.dll
  - msvcr80.dll
  - msvcr120.dll
  - msvcr110.dll
  - msvcr100.dll
  - msvcrt.dll
  - msvcr110_clr0400.dll
apitype: DLLExport
ms.assetid: 312ae3e6-278c-459a-9393-11b8f87d9184
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# rint, rintf, rintl
Rounds a floating-point value to the nearest integer in floating-point format.  
  
## Syntax  
  
```  
double rint( double x );  
float rint( float x );  // C++ only  
long double rint( long double x );  // C++ only  
float rintf( float x );   
long double rintl( long double x );  
  
```  
  
#### Parameters  
 `x`  
 The floating-point value to round.  
  
## Return Value  
 The `rint` functions return a floating-point value that represents the nearest integer to `x`. Halfway values are rounded according to the current setting of the floating-point rounding mode, the same as the `nearbyint` functions. Unlike the `nearbyint` functions, the `rint` functions may raise the `FE_INEXACT` floating-point exception if the result differs in value from the argument. There is no error return.  
  
|Input|SEH Exception|`_matherr` Exception|  
|-----------|-------------------|--------------------------|  
|± ∞, QNAN, IND|none|none|  
|Denormals|EXCEPTION_FLT_UNDERFLOW|none|  
  
## Remarks  
 Because C++ allows overloading, you can call overloads of `rint` that take and return `float` and `long double` values. In a C program, `rint` always takes and returns a `double`.  
  
## Requirements  
  
|Function|C header|C++ header|  
|--------------|--------------|------------------|  
|`rint`, `rintf`, `rintl`|<math.h>|<cmath\>|  
  
 For additional compatibility information, see [Compatibility](../vs140/Compatibility.md).  
  
## Example  
  
```  
// crt_rint.c  
// Build with: cl /W3 /Tc crt_rint.c  
// This example displays the rounded results of  
// the floating-point values 2.499999, -2.499999,   
// 2.8, -2.8, 2.5 and -2.5.  
  
#include <math.h>  
#include <stdio.h>  
  
int main( void )  
{  
   double x = 2.499999;  
   float y = 2.8f;  
   long double z = 2.5;  
  
   printf("rint(%f) is %.0f\n", x, rint (x));  
   printf("rint(%f) is %.0f\n", -x, rint (-x));  
   printf("rintf(%f) is %.0f\n", y, rintf(y));  
   printf("rintf(%f) is %.0f\n", -y, rintf(-y));  
   printf("rintl(%Lf) is %.0Lf\n", z, rintl(z));  
   printf("rintl(%Lf) is %.0Lf\n", -z, rintl(-z));  
}  
```  
  
 **rint(2.499999) is 2**  
**rint(-2.499999) is -2**  
**rintf(2.800000) is 3**  
**rintf(-2.800000) is -3**  
**rintl(2.500000) is 3**  
**rintl(-2.500000) is -3**   
## .NET Framework Equivalent  
 [System::Math::Round](https://msdn.microsoft.com/en-us/library/system.math.round.aspx)  
  
## See Also  
 [Floating-Point Support](../vs140/Floating-Point-Support.md)   
 [ceil](../vs140/ceil--ceilf--ceill.md)   
 [floor, floorf, floorl](../vs140/floor--floorf--floorl.md)   
 [fmod, fmodf](../vs140/fmod--fmodf.md)   
 [lrint, lrintf, lrintl, llrint, llrintf, llrintl](assetId:///312fd869-a9c0-4107-bb23-ab8299d04385)   
 [lround](../vs140/lround--lroundf--lroundl--llround--llroundf--llroundl.md)   
 [nearbyint, nearbyintf, nearbyintl](assetId:///15111e73-331d-41d1-81b7-3e10df894848)   
 [rint](../vs140/rint--rintf--rintl.md)