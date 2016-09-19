---
title: "_cabs"
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
  - _cabs
apilocation: 
  - msvcr120.dll
  - msvcr80.dll
  - msvcr100.dll
  - msvcrt.dll
  - msvcr90.dll
  - msvcr110.dll
  - msvcr110_clr0400.dll
apitype: DLLExport
ms.assetid: fea292ee-1a39-4a0a-b416-4a189346ff26
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _cabs
Calculates the absolute value of a complex number.  
  
## Syntax  
  
```  
double _cabs(   
   struct _complex z   
);  
```  
  
#### Parameters  
 `z`  
 Complex number.  
  
## Return Value  
 `_cabs` returns the absolute value of its argument if successful. On overflow, `_cabs` returns `HUGE_VAL` and sets `errno` to `ERANGE`. You can change error handling with [_matherr](../vs140/_matherr.md).  
  
## Remarks  
 The `_cabs` function calculates the absolute value of a complex number, which must be a structure of type [_complex](../vs140/Standard-Types.md). The structure `z` is composed of a real component `x` and an imaginary component `y`. A call to `_cabs` produces a value equivalent to that of the expression `sqrt`( `z.x``*``z.x``+``z.y`*`z.y` ).  
  
## Requirements  
  
|Routine|Required header|  
|-------------|---------------------|  
|`_cabs`|<math.h>|  
  
 For more compatibility information, see [Compatibility](../vs140/Compatibility.md) in the Introduction.  
  
## Example  
  
```  
// crt_cabs.c  
/* Using _cabs, this program calculates  
 * the absolute value of a complex number.  
 */  
#include <math.h>  
#include <stdio.h>  
  
int main( void )  
{  
   struct _complex number = { 3.0, 4.0 };  
   double d;  
  
   d = _cabs( number );  
   printf( "The absolute value of %f + %fi is %f\n",  
           number.x, number.y, d );  
}  
```  
  
 **The absolute value of 3.000000 + 4.000000i is 5.000000**   
## .NET Framework Equivalent  
 Not applicable. To call the standard C function, use `PInvoke`. For more information, see [Platform Invoke Examples](assetId:///15926806-f0b7-487e-93a6-4e9367ec689f).  
  
## See Also  
 [Floating-Point Support](../vs140/Floating-Point-Support.md)   
 [abs, labs, llabs, _abs64](../vs140/abs--labs--llabs--_abs64.md)   
 [fabs, fabsf, fabsl](../vs140/fabs--fabsf--fabsl.md)   
 [labs, llabs](../vs140/labs--llabs.md)