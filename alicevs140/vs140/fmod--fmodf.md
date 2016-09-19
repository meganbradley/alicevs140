---
title: "fmod, fmodf"
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
  - fmod
  - fmodf
apilocation: 
  - msvcr100.dll
  - msvcrt.dll
  - msvcr110_clr0400.dll
  - msvcr110.dll
  - msvcr120.dll
  - msvcr90.dll
  - msvcr80.dll
apitype: DLLExport
ms.assetid: 6962d369-d11f-40b1-a6d7-6f67239f8a23
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# fmod, fmodf
Calculates the floating-point remainder.  
  
## Syntax  
  
```  
double fmod(   
   double x,  
   double y   
);  
float fmod(  
   float x,  
   float y   
);  // C++ only  
long double fmod(  
   long double x,  
   long double y  
);  // C++ only  
float fmodf(   
   float x,  
   float y   
);  
```  
  
#### Parameters  
 `x`, `y`  
 Floating-point values.  
  
## Return Value  
 `fmod` returns the floating-point remainder of `x` / `y`. If the value of `y` is 0.0, `fmod` returns a quiet NaN. For information about representation of a quiet NaN by the `printf` family, see [printf](../vs140/printf--_printf_l--wprintf--_wprintf_l.md).  
  
## Remarks  
 The `fmod` function calculates the floating-point remainder `f` of `x` / `y` such that `x` = `i` `*` `y` + `f`, where `i` is an integer, `f` has the same sign as `x`, and the absolute value of `f` is less than the absolute value of `y`.  
  
 C++ allows overloading, so you can call overloads of `fmod`. In a C program, `fmod` always takes two doubles and returns a double.  
  
## Requirements  
  
|Function|Required header|  
|--------------|---------------------|  
|`fmod`, `fmodf`|<math.h>|  
  
 For additional compatibility information, see [Compatibility](../vs140/Compatibility.md) in the Introduction.  
  
## Example  
  
```  
// crt_fmod.c  
// This program displays a floating-point remainder.  
  
#include <math.h>  
#include <stdio.h>  
  
int main( void )  
{  
   double w = -10.0, x = 3.0, z;  
  
   z = fmod( w, x );  
   printf( "The remainder of %.2f / %.2f is %f\n", w, x, z );  
}  
```  
  
 **The remainder of -10.00 / 3.00 is -1.000000**   
## .NET Framework Equivalent  
 [System::Math::IEEERemainder](https://msdn.microsoft.com/en-us/library/system.math.ieeeremainder.aspx)  
  
## See Also  
 [Floating-Point Support](../vs140/Floating-Point-Support.md)   
 [ceil, ceilf, ceill](../vs140/ceil--ceilf--ceill.md)   
 [fabs, fabsf, fabsl](../vs140/fabs--fabsf--fabsl.md)   
 [floor, floorf, floorl](../vs140/floor--floorf--floorl.md)   
 [_CIfmod](../vs140/_CIfmod.md)