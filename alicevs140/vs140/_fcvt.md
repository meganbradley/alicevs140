---
title: "_fcvt"
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
  - _fcvt
apilocation: 
  - msvcr120.dll
  - msvcrt.dll
  - msvcr110.dll
  - msvcr90.dll
  - msvcr80.dll
  - msvcr100.dll
  - msvcr110_clr0400.dll
apitype: DLLExport
ms.assetid: 74584c88-f0dd-4907-8fca-52da5df583f5
caps.latest.revision: 24
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _fcvt
Converts a floating-point number to a string. A more secure version of this function is available; see [_fcvt_s](../Topic/_fcvt_s.md).  
  
## Syntax  
  
```  
char *_fcvt(   
   double value,  
   int count,  
   int *dec,  
   int *sign   
);  
```  
  
#### Parameters  
 `value`  
 Number to be converted.  
  
 `count`  
 Number of digits after the decimal point.  
  
 `dec`  
 Pointer to the stored decimal-point position.  
  
 `sign`  
 Pointer to the stored sign indicator.  
  
## Return Value  
 `_fcvt` returns a pointer to the string of digits, NULL on error.  
  
## Remarks  
 The `_fcvt` function converts a floating-point number to a null-terminated character string. The `value` parameter is the floating-point number to be converted. `_fcvt` stores the digits of `value` as a string and appends a null character ('\0'). The `count` parameter specifies the number of digits to be stored after the decimal point. Excess digits are rounded off to `count` places. If there are fewer than `count` digits of precision, the string is padded with zeros.  
  
 The total number of digits returned by `_fcvt` will not exceed `_CVTBUFSIZE`.  
  
 Only digits are stored in the string. The position of the decimal point and the sign of `value` can be obtained from `dec` and sign after the call. The `dec` parameter points to an integer value; this integer value gives the position of the decimal point with respect to the beginning of the string. A zero or negative integer value indicates that the decimal point lies to the left of the first digit. The parameter `sign` points to an integer indicating the sign of `value`. The integer is set to 0 if `value` is positive and is set to a nonzero number if `value` is negative.  
  
 The difference between `_ecvt` and `_fcvt` is in the interpretation of the `count` parameter. `_ecvt` interprets `count` as the total number of digits in the output string, whereas `_fcvt` interprets `count` as the number of digits after the decimal point.  
  
 `_ecvt` and `_fcvt` use a single statically allocated buffer for the conversion. Each call to one of these routines destroys the results of the previous call.  
  
 This function validates its parameters. If `dec` or `sign` is NULL, or `count` is 0, the invalid parameter handler is invoked, as described in [Parameter Validation](../vs140/Parameter-Validation.md). If execution is allowed to continue, `errno` is set to `EINVAL` and NULL is returned.  
  
## Requirements  
  
|Function|Required header|  
|--------------|---------------------|  
|`_fcvt`|<stdlib.h>|  
  
 For more compatibility information, see [Compatibility](../vs140/Compatibility.md) in the Introduction.  
  
## Example  
  
```  
// crt_fcvt.c  
// compile with: /W3  
// This program converts the constant  
// 3.1415926535 to a string and sets the pointer  
// buffer to point to that string.  
  
#include <stdlib.h>  
#include <stdio.h>  
  
int main( void )  
{  
   int  decimal, sign;  
   char *buffer;  
   double source = 3.1415926535;  
  
   buffer = _fcvt( source, 7, &decimal, &sign ); // C4996  
   // Note: _fcvt is deprecated; consider using _fcvt_s instead  
   printf( "source: %2.10f   buffer: '%s'   decimal: %d   sign: %d\n",  
            source, buffer, decimal, sign );  
}  
```  
  
 **source: 3.1415926535   buffer: '31415927'   decimal: 1   sign: 0**   
## .NET Framework Equivalent  
 [System::Convert::ToString](https://msdn.microsoft.com/en-us/library/system.convert.tostring.aspx)  
  
## See Also  
 [Data Conversion](../vs140/Data-Conversion.md)   
 [Floating-Point Support](../vs140/Floating-Point-Support.md)   
 [atof, _atof_l, _wtof, _wtof_l](../vs140/atof--_atof_l--_wtof--_wtof_l.md)   
 [_ecvt](../vs140/_ecvt.md)   
 [_gcvt](../vs140/_gcvt.md)