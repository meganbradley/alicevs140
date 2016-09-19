---
title: "cos, cosf, cosl, cosh, coshf, coshl"
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
  - coshl
  - cosh
  - cos
  - cosl
  - cosf
  - coshf
apilocation: 
  - msvcr110_clr0400.dll
  - msvcr80.dll
  - msvcr120.dll
  - msvcrt.dll
  - msvcr90.dll
  - msvcr100.dll
  - msvcr110.dll
apitype: DLLExport
ms.assetid: ae90435e-6b68-4a47-a81f-be87d5c08f16
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# cos, cosf, cosl, cosh, coshf, coshl
Calculates the cosine (`cos`, `cosf`, or `cosl`), or hyperbolic cosine (`cosh`, `coshf`, or `coshl`).  
  
## Syntax  
  
```  
double cos(   
   double x   
);  
float cos(  
   float x   
);  // C++ only  
long double cos(  
   long double x  
);  // C++ only  
float cosf(   
   float x   
);  
long double cosl(  
   long double x  
);  
double cosh(   
   double x   
);  
float cosh(  
   float x   
);  // C++ only  
long double cosh(  
   long double x  
);  // C++ only  
float coshf(  
   float x   
);  
long double coshl(  
   long double x  
);  
```  
  
#### Parameters  
 `x`  
 Angle in radians.  
  
## Return Value  
 The cosine or hyperbolic cosine of `x`. If `x` is greater than or equal to 263, or less than or equal to –263, a loss of significance in the result of a call to `cos`, `cosf`, or `cosl` occurs.  
  
 By default, if the result is too large in a `cosh`, `coshf`, or `coshl` call, the function returns `HUGE_VAL` and sets `errno` to `ERANGE`.  
  
|Input|SEH Exception|Matherr Exception|  
|-----------|-------------------|-----------------------|  
|± `QNAN`,`IND`|none|`_DOMAIN`|  
|± ∞  (`cosf`, `cos`, `cosl`)|`INVALID`|`_DOMAIN`|  
|x ≥ 7.104760e+002  (`cosh`, `coshf`, `coshl`)|`INEXACT`+`OVERFLOW`|`OVERFLOW`|  
  
## Remarks  
 Because C++ allows overloading, you can call overloads of `cos` and `cosh` that take and return `float` or `long double` values. In a C program, `cos` and `cosh` always take and return a `double`.  
  
## Requirements  
  
|Routine|Required header|  
|-------------|---------------------|  
|`cos`, `cosh`, `cosf`, `coshf`, `cosl`, `coshl`|<math.h>|  
  
 For additional compatibility information, see [Compatibility](../vs140/Compatibility.md).  
  
## Example  
 See the example in [sin, sinf, sinl, sinh, sinhf, sinhl](../vs140/sin--sinf--sinl--sinh--sinhf--sinhl.md).  
  
## .NET Framework Equivalent  
  
-   [System::Math::Cos](https://msdn.microsoft.com/en-us/library/system.math.cos.aspx)  
  
-   [System::Math::Cosh](https://msdn.microsoft.com/en-us/library/system.math.cosh.aspx)  
  
## See Also  
 [Floating-Point Support](../vs140/Floating-Point-Support.md)   
 [acos, acosf, acosl](../vs140/acos--acosf--acosl.md)   
 [asin, asinf, asinl](../vs140/asin--asinf--asinl.md)   
 [atan, atanf, atanl, atan2, atan2f, atan2l](../vs140/atan--atanf--atanl--atan2--atan2f--atan2l.md)   
 [_matherr](../vs140/_matherr.md)   
 [sin, sinf, sinl, sinh, sinhf, sinhl](../vs140/sin--sinf--sinl--sinh--sinhf--sinhl.md)   
 [tan, tanf, tanl, tanh, tanhf, tanhl](../vs140/tan--tanf--tanl--tanh--tanhf--tanhl.md)   
 [_CIcos](../vs140/_CIcos.md)