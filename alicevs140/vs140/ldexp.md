---
title: "ldexp"
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
  - ldexp
apilocation: 
  - msvcr100.dll
  - msvcr110.dll
  - msvcr90.dll
  - msvcrt.dll
  - msvcr80.dll
  - msvcr120.dll
  - msvcr110_clr0400.dll
apitype: DLLExport
ms.assetid: aa7f5310-3879-4f63-ae74-86a39fbdedfa
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ldexp
Multiplies a floating-point number by an integral power of two.  
  
## Syntax  
  
```  
double ldexp(  
   double x,  
   int exp   
);  
float ldexp(  
   float x,  
   int exp  
);  // C++ only  
long double ldexp(  
   long double x,  
   int exp  
);  // C++ only   
float ldexpf(  
   float x,  
   int exp  
);   
long double ldexpl(  
   long double x,  
   int exp  
);   
```  
  
#### Parameters  
 `x`  
 Floating-point value.  
  
 `exp`  
 Integer exponent.  
  
## Return Value  
 The `ldexp` function returns the value of `x` * 2<sup>exp</sup> if successful. On overflow, and depending on the sign of `x`, `ldexp` returns +/– `HUGE_VAL`; the `errno` value is set to `ERANGE`.  
  
 For more information about `errno` and possible error return values, see [errno, _doserrno, _sys_errlist, and _sys_nerr](../vs140/errno--_doserrno--_sys_errlist--and-_sys_nerr.md).  
  
## Remarks  
 Because C++ allows overloading, you can call overloads of `ldexp` that take `float` or `long double` types. In a C program, `ldexp` always takes a `double` and an `int` and returns a `double`.  
  
## Requirements  
  
|Routine|C header|C++ header|  
|-------------|--------------|------------------|  
|`ldexp`, `ldexpf`, `ldexpl`|<math.h>|<cmath\>|  
  
 For compatibility information, see [Compatibility](../vs140/Compatibility.md).  
  
## Example  
  
```  
// crt_ldexp.c  
  
#include <math.h>  
#include <stdio.h>  
  
int main( void )  
{  
   double x = 4.0, y;  
   int p = 3;  
  
   y = ldexp( x, p );  
   printf( "%2.1f times two to the power of %d is %2.1f\n", x, p, y );  
}  
```  
  
## Output  
  
```  
4.0 times two to the power of 3 is 32.0  
```  
  
## .NET Framework Equivalent  
 [System::Math::Pow](https://msdn.microsoft.com/en-us/library/system.math.pow.aspx)  
  
## See Also  
 [Floating-Point Support](../vs140/Floating-Point-Support.md)   
 [frexp](../vs140/frexp.md)   
 [modf, modff, modfl](../vs140/modf--modff--modfl.md)