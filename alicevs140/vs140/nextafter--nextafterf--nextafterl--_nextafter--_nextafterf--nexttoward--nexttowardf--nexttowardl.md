---
title: "nextafter, nextafterf, nextafterl, _nextafter, _nextafterf, nexttoward, nexttowardf, nexttowardl"
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
  - nextafterf
  - _nextafterf
  - nextafter
  - nextafterl
  - _nextafter
  - nexttoward
  - nexttowardf
  - nexttowardl
apilocation: 
  - msvcr120.dll
  - msvcr100.dll
  - msvcr80.dll
  - msvcr90.dll
  - msvcr110_clr0400.dll
  - msvcrt.dll
  - msvcr110.dll
  - api-ms-win-crt-math-l1-1-0.dll
apitype: DLLExport
ms.assetid: 9785bfb9-de53-4bd0-9637-f05fa0c1f6ab
caps.latest.revision: 15
translation.priority.mt: 
  - de-de
  - ja-jp
---
# nextafter, nextafterf, nextafterl, _nextafter, _nextafterf, nexttoward, nexttowardf, nexttowardl
Returns the next representable floating-point value.  
  
## Syntax  
  
```  
double nextafter(  
   double x,  
   double y   
);  
  
float nextafter(  
   float x,  
   float y   
); /* C++ only, requires <cmath> */  
  
long double nextafter(  
   long double x,  
   long double y   
); /* C++ only, requires <cmath> */  
  
float nextafterf(  
   float x,  
   float y   
);   
  
long double nextafterl(  
   long double x,  
   long double y   
);  
  
double _nextafter(  
   double x,  
   double y   
);  
  
float _nextafterf(  
   float x,  
   float y   
); /* x64 only */  
  
double nexttoward(  
   double x,  
   long double y   
);  
  
float nexttoward(  
   float x,  
   long double y   
); /* C++ only, requires <cmath> */  
  
long double nexttoward(  
   long double x,  
   long double y   
); /* C++ only, requires <cmath> */  
  
float nexttowardf(  
   float x,  
   long double y   
);   
  
long double nexttowardl(  
   long double x,  
   long double y   
);  
```  
  
#### Parameters  
 `x`  
 The floating-point value to start from.  
  
 `y`  
 The floating-point value to go towards.  
  
## Return Value  
 Returns the next representable floating-point value of the return type after `x` in the direction of `y`. If `x`=`y`, the function returns `y`, converted to the return type, with no exception triggered. If `x` is not equal to `y`, and the result is a denormal or zero, the FE_UNDERFLOW and FE_INEXACT floating-point exception states are set, and the correct result is returned. If either `x` or `y` is a NAN, then the return value is one of the input NANs. If `x` is finite and the result is infinite or not representable in the type, a correctly signed infinity or NAN is returned, the FE_OVERFLOW and FE_INEXACT floating-point exception states are set, and `errno` is set to ERANGE.  
  
## Remarks  
 The `nextafter` and `nexttoward` function families are equivalent, except for the parameter type of `y`. If `x` and `y` are equal, the value returned is `y` converted to the return type.  
  
 Because C++ allows overloading, if you include <cmath\> you can call overloads of `nextafter` and `nexttoward` that return `float` and `long double` types. In a C program, `nextafter` and `nexttoward` always return `double`.  
  
 The `_nextafter` and `_nextafterf` functions are Microsoft specific. The `_nextafterf` function is only available when compiling for x64.  
  
## Requirements  
  
|Routine|Required header (C)|Required header (C++)|  
|-------------|---------------------------|-------------------------------|  
|`nextafter`, `nextafterf`, `nextafterl`, `_nextafterf`, `nexttoward`, `nexttowardf`, `nexttowardl`|<math.h>|<math.h> or <cmath\>|  
|`_nextafter`|<float.h>|<float.h> or <cfloat\>|  
  
 For more compatibility information, see [Compatibility](../vs140/Compatibility.md) in the Introduction.  
  
## See Also  
 [Floating-Point Support](../vs140/Floating-Point-Support.md)   
 [isnan, _isnan, _isnanf](../vs140/isnan--_isnan--_isnanf.md)