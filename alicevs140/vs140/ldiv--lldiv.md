---
title: "ldiv, lldiv"
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
  - ldiv
  - lldiv
apilocation: 
  - msvcr110_clr0400.dll
  - msvcrt.dll
  - msvcr100.dll
  - msvcr90.dll
  - msvcr80.dll
  - msvcr120.dll
  - msvcr110.dll
apitype: DLLExport
ms.assetid: 68ab5d83-27a4-479c-9d52-d055eb139eca
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ldiv, lldiv
Computes the quotient and remainder of two integers as one operation.  
  
## Syntax  
  
```  
ldiv_t ldiv(  
   long numer,  
   long denom   
);  
lldiv_t lldiv(  
   long long numer,  
   long long denom   
);  
```  
  
#### Parameters  
 `numer`  
 Numerator.  
  
 `denom`  
 Denominator.  
  
## Return Value  
 `ldiv` returns a structure of type [ldiv_t](../vs140/Standard-Types.md) that comprises both the quotient and the remainder. `lldiv` returns a structure of type [lldiv_t](../vs140/Standard-Types.md) that comprises both the quotient and the remainder.  
  
## Remarks  
 The `ldiv` and `lldiv` functions divide `numer` by `denom`, and thereby compute the quotient and remainder. The sign of the quotient is the same as that of the mathematical quotient. The absolute value of the quotient is the largest integer that is less than the absolute value of the mathematical quotient. If the denominator is 0, the program terminates with an error message. `ldiv` and `lldiv` are the same as `div`, except that the arguments of `ldiv` and the members of the returned structure are all of type `long`, and the arguments of `lldiv` and the members of the returned structure are of type `long long`.  
  
 The `ldiv_t` and `lldiv_t` structures are defined in <stdlib.h>.  
  
## Requirements  
  
|Routine|Required header|  
|-------------|---------------------|  
|`ldiv`, `lldiv`|<stdlib.h>|  
  
 For additional compatibility information, see [Compatibility](../vs140/Compatibility.md).  
  
## Libraries  
 All versions of the [C run-time libraries](../vs140/CRT-Library-Features.md).  
  
## Example  
  
```  
// crt_ldiv.c  
  
#include <stdlib.h>  
#include <math.h>  
#include <stdio.h>  
  
int main( void )  
{  
   long x = 5149627, y = 234879;  
   ldiv_t div_result;  
  
   div_result = ldiv( x, y );  
   printf( "For %ld / %ld, the quotient is ", x, y );  
   printf( "%ld, and the remainder is %ld\n",   
            div_result.quot, div_result.rem );  
}  
```  
  
## Output  
  
```  
For 5149627 / 234879, the quotient is 21, and the remainder is 217168  
```  
  
## .NET Framework Equivalent  
 Not applicable. To call the standard C function, use `PInvoke`. For more information, see [Platform Invoke Examples](assetId:///15926806-f0b7-487e-93a6-4e9367ec689f).  
  
## See Also  
 [Floating-Point Support](../vs140/Floating-Point-Support.md)   
 [div](../vs140/div.md)   
 [imaxdiv](../vs140/imaxdiv.md)