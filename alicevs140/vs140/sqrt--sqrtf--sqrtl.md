---
title: "sqrt, sqrtf, sqrtl"
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
  - sqrtl
  - sqrtf
  - sqrt
apilocation: 
  - msvcr110.dll
  - msvcr80.dll
  - msvcr110_clr0400.dll
  - msvcr100.dll
  - msvcrt.dll
  - msvcr120.dll
  - msvcr90.dll
apitype: DLLExport
ms.assetid: 2ba9467b-f172-41dc-8f10-b86f68fa813c
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# sqrt, sqrtf, sqrtl
Calculates the square root.  
  
## Syntax  
  
```  
double sqrt(  
   double x   
);  
float sqrt(  
   float x   
);  // C++ only  
long double sqrt(  
   long double x  
);  // C++ only  
float sqrtf(  
   float x   
);  
long double sqrtl(  
   long double x   
);  
```  
  
#### Parameters  
 `x`  
 Non-negative floating-point value  
  
## Remarks  
 Because C++ allows overloading, you can call overloads of `sqrt` that take `float` or `long double` types. In a C program, `sqrt` always takes and returns `double`.  
  
## Return Value  
 The `sqrt` functions return the square-root of `x`. By default, if `x` is negative, `sqrt` returns an indefinite NaN.  
  
|Input|SEH Exception|`_matherr` Exception|  
|-----------|-------------------|--------------------------|  
|± QNAN,IND|none|_DOMAIN|  
|- ∞|none|_DOMAIN|  
|x<0|none|_DOMAIN|  
  
## Requirements  
  
|Function|C header|C++ header|  
|--------------|--------------|------------------|  
|`sqrt`, `sqrtf`, `sqrtl`|<math.h>|<cmath\>|  
  
 For compatibility information, see [Compatibility](../vs140/Compatibility.md).  
  
## Example  
  
```  
// crt_sqrt.c  
// This program calculates a square root.  
  
#include <math.h>  
#include <stdio.h>  
#include <stdlib.h>  
  
int main( void )  
{  
   double question = 45.35, answer;  
   answer = sqrt( question );  
   if( question < 0 )  
      printf( "Error: sqrt returns %f\n", answer );  
   else  
      printf( "The square root of %.2f is %.2f\n", question, answer );  
}  
```  
  
 **The square root of 45.35 is 6.73**   
## .NET Framework Equivalent  
 [System::Math::Sqrt](https://msdn.microsoft.com/en-us/library/system.math.sqrt.aspx)  
  
## See Also  
 [Floating-Point Support](../vs140/Floating-Point-Support.md)   
 [exp, expf](../vs140/exp--expf.md)   
 [log, logf, log10, log10f](../vs140/log--logf--log10--log10f.md)   
 [pow, powf, powl](../vs140/pow--powf--powl.md)   
 [_CIsqrt](../vs140/_CIsqrt.md)