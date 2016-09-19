---
title: "log, logf, log10, log10f"
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
  - log10f
  - logf
  - log10
  - log
apilocation: 
  - msvcr80.dll
  - msvcrt.dll
  - msvcr100.dll
  - msvcr120.dll
  - msvcr110_clr0400.dll
  - msvcr110.dll
  - msvcr90.dll
apitype: DLLExport
ms.assetid: 7adc77c2-04f7-4245-a980-21215563cfae
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# log, logf, log10, log10f
Calculates logarithms.  
  
## Syntax  
  
```  
  
      double log(  
   double x   
);  
float log(  
   float x  
);  // C++ only  
long double log(  
   long double x  
);  // C++ only  
float logf(  
   float x   
);  
double log10(  
   double x  
);  
float log10(  
   float x  
);  // C++ only  
long double log10(  
   long double x  
);  // C++ only  
float log10f (  
   float x  
);  
```  
  
#### Parameters  
 *x*  
 Value whose logarithm is to be found.  
  
## Return Value  
 The **log** functions return the natural logarithm (base e) of *x* if successful. The log10 functions return the base-10 logarithm. If *x* is negative, these functions return an indefinite, by default. If *x* is 0, they return INF (infinite).  
  
|Input|SEH Exception|Matherr Exception|  
|-----------|-------------------|-----------------------|  
|± QNAN,IND|none|_DOMAIN|  
|± 0|ZERODIVIDE|_SING|  
|x < 0|INVALID|_DOMAIN|  
  
 **log** and `log10` has an implementation that uses Streaming SIMD Extensions 2 (SSE2). See [_set_SSE2_enable](../vs140/_set_SSE2_enable.md) for information and restrictions on using the SSE2 implementation.  
  
## Remarks  
 C++ allows overloading, so you can call overloads of **log** and `log10`. In a C program, **log** and `log10` always take and return a double.  
  
## Requirements  
  
|Routine|Required header|  
|-------------|---------------------|  
|**log**, `logf`, `log10`, `log10f`|<math.h>|  
  
 For additional compatibility information, see [Compatibility](../vs140/Compatibility.md) in the Introduction.  
  
## Libraries  
 All versions of the [C run-time libraries](../vs140/CRT-Library-Features.md).  
  
## Example  
  
```  
// crt_log.c  
/* This program uses log and log10  
 * to calculate the natural logarithm and  
 * the base-10 logarithm of 9,000.  
 */  
  
#include <math.h>  
#include <stdio.h>  
  
int main( void )  
{  
   double x = 9000.0;  
   double y;  
  
   y = log( x );  
   printf( "log( %.2f ) = %f\n", x, y );  
   y = log10( x );  
   printf( "log10( %.2f ) = %f\n", x, y );  
}  
```  
  
## Output  
  
```  
log( 9000.00 ) = 9.104980  
log10( 9000.00 ) = 3.954243  
```  
  
 To generate logarithms for other bases, use the mathematical relation: log base b of a == natural log (a) / natural log (b).  
  
```  
// logbase.cpp  
#include <math.h>  
#include <stdio.h>  
  
double logbase(double a, double base)  
{  
   return log(a) / log(base);  
}  
  
int main()  
{  
   double x = 65536;  
   double result;  
  
   result = logbase(x, 2);  
   printf("Log base 2 of %lf is %lf\n", x, result);  
}  
```  
  
## Output  
  
```  
Log base 2 of 65536.000000 is 16.000000  
```  
  
## .NET Framework Equivalent  
  
-   [System::Math::Log](https://msdn.microsoft.com/en-us/library/system.math.log.aspx)  
  
-   [System::Math::Log10](https://msdn.microsoft.com/en-us/library/system.math.log10.aspx)  
  
## See Also  
 [Floating-Point Support](../vs140/Floating-Point-Support.md)   
 [exp, expf](../vs140/exp--expf.md)   
 [_matherr](../vs140/_matherr.md)   
 [pow, powf, powl](../vs140/pow--powf--powl.md)   
 [_CIlog](../vs140/_CIlog.md)   
 [_CIlog10](../vs140/_CIlog10.md)