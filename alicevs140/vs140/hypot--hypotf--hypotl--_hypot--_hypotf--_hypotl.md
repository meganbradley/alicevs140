---
title: "hypot, hypotf, hypotl, _hypot, _hypotf, _hypotl"
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
  - _hypotf
  - hypot
  - hypotf
  - _hypot
  - _hypotl
  - hypotl
apilocation: 
  - msvcr120.dll
  - msvcr110.dll
  - msvcr100.dll
  - msvcr90.dll
  - msvcr110_clr0400.dll
  - msvcrt.dll
  - msvcr80.dll
apitype: DLLExport
ms.assetid: 6a13887f-bd53-43fc-9d77-5b42d6e49925
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# hypot, hypotf, hypotl, _hypot, _hypotf, _hypotl
Calculates the hypotenuse.  
  
## Syntax  
  
```  
double hypot(   
   double x,  
   double y   
);  
float hypotf(   
   float x,  
   float y   
);  
long double hypotl(  
   long double x,  
   long double y  
);  
double _hypot(   
   double x,  
   double y   
);  
float _hypotf(   
   float x,  
   float y   
);  
long double _hypotl(  
   long double x,  
   long double y  
);  
```  
  
#### Parameters  
 `x`, `y`  
 Floating-point values.  
  
## Return Value  
 If successful, `hypot` returns the length of the hypotenuse; on overflow, `hypot` returns INF (infinity) and the `errno` variable is set to `ERANGE`. You can use `_matherr` to modify error handling.  
  
 For more information about return codes, see [errno, _doserrno, _sys_errlist, and _sys_nerr](../vs140/errno--_doserrno--_sys_errlist--and-_sys_nerr.md).  
  
## Remarks  
 The `hypot` functions calculate the length of the hypotenuse of a right triangle, given the length of the two sides `x` and `y` (in other words, the square root of `x`<sup>2</sup> + `y`<sup>2</sup>).  
  
 The versions of the functions that have leading underscores are provided for compatibility with earlier standards. Their behavior is identical to the versions that don't have leading underscores. We recommend using the versions without leading underscores for new code.  
  
## Requirements  
  
|Routine|Required header|  
|-------------|---------------------|  
|`hypot`, `hypotf`, `hypotl`, `_hypot`, `_hypotf`, `_hypotl`|<math.h>|  
  
 For more compatibility information, see [Compatibility](../vs140/Compatibility.md).  
  
## Example  
  
```  
// crt_hypot.c  
// This program prints the hypotenuse of a right triangle.  
  
#include <math.h>  
#include <stdio.h>  
  
int main( void )  
{  
   double x = 3.0, y = 4.0;  
  
   printf( "If a right triangle has sides %2.1f and %2.1f, "  
           "its hypotenuse is %2.1f\n", x, y, _hypot( x, y ) );  
}  
```  
  
 **If a right triangle has sides 3.0 and 4.0, its hypotenuse is 5.0**   
## .NET Framework Equivalent  
 Not applicable. To call the standard C function, use `PInvoke`. For more information, see [Platform Invoke Examples](assetId:///15926806-f0b7-487e-93a6-4e9367ec689f).  
  
## See Also  
 [Floating-Point Support](../vs140/Floating-Point-Support.md)   
 [_cabs](../vs140/_cabs.md)   
 [_matherr](../vs140/_matherr.md)