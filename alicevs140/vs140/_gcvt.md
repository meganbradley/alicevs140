---
title: "_gcvt"
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
  - _gcvt
apilocation: 
  - msvcr110_clr0400.dll
  - msvcr100.dll
  - msvcrt.dll
  - msvcr80.dll
  - msvcr120.dll
  - msvcr90.dll
  - msvcr110.dll
apitype: DLLExport
ms.assetid: 5761411e-c06b-409a-912f-810fe7f4bcb5
caps.latest.revision: 25
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _gcvt
Converts a floating-point value to a string, which it stores in a buffer. A more secure version of this function is available; see [_gcvt_s](../Topic/_gcvt_s.md).  
  
## Syntax  
  
```  
char *_gcvt(   
   double value,  
   int digits,  
   char *buffer   
);  
```  
  
#### Parameters  
 `value`  
 Value to be converted.  
  
 `digits`  
 Number of significant digits stored.  
  
 `buffer`  
 Storage location for the result.  
  
## Return Value  
 `_gcvt` returns a pointer to the string of digits.  
  
## Remarks  
 The `_gcvt` function converts a floating-point `value` to a character string (which includes a decimal point and a possible sign byte) and stores the string in `buffer`. The `buffer` should be large enough to accommodate the converted value plus a terminating null character, which is appended automatically. If a buffer size of `digits` + 1 is used, the function overwrites the end of the buffer. This is because the converted string includes a decimal point and can contain sign and exponent information. There is no provision for overflow. `_gcvt` attempts to produce `digits` digits in decimal format. If it cannot, it produces `digits` digits in exponential format. Trailing zeros might be suppressed in the conversion.  
  
 A `buffer` of length `_CVTBUFSIZE` is sufficient for any floating point value.  
  
 This function validates its parameters. If `buffer` is `NULL`, the invalid parameter handler is invoked, as described in [Parameter Validation](../vs140/Parameter-Validation.md). If execution is allowed to continue, this function sets `errno` to `EINVAL` and returns `NULL`.  
  
## Requirements  
  
|Routine|Required header|  
|-------------|---------------------|  
|`_gcvt`|<stdlib.h>|  
  
 For more compatibility information, see [Compatibility](../vs140/Compatibility.md) in the Introduction.  
  
## Example  
  
```  
// crt_gcvt.c  
// compile with: /W3  
#include <stdlib.h>  
#include <stdio.h>  
#include <string.h>  
  
int main( void )  
{  
   char buffer[_CVTBUFSIZE];  
   double value = -1234567890.123;  
   printf( "The following numbers were converted by _gcvt(value,12,buffer):\n" );  
   _gcvt( value, 12, buffer ); // C4996  
   // Note: _gcvt is deprecated; consider using _gcvt_s instead  
   printf( "buffer: '%s' (%d chars)\n", buffer, strlen(buffer) );  
   value *= 10;  
   _gcvt( value, 12, buffer ); // C4996  
   printf( "buffer: '%s' (%d chars)\n", buffer, strlen(buffer) );  
   value *= 10;  
   _gcvt( value, 12, buffer ); // C4996  
   printf( "buffer: '%s' (%d chars)\n", buffer, strlen(buffer) );  
   value *= 10;  
   _gcvt( value, 12, buffer ); // C4996  
   printf( "buffer: '%s' (%d chars)\n", buffer, strlen(buffer) );  
  
   printf( "\n" );  
   value = -12.34567890123;  
   _gcvt( value, 12, buffer ); // C4996  
   printf( "buffer: '%s' (%d chars)\n", buffer, strlen(buffer) );  
   value /= 10;  
   _gcvt( value, 12, buffer ); // C4996  
   printf( "buffer: '%s' (%d chars)\n", buffer, strlen(buffer) );  
   value /= 10;  
   _gcvt( value, 12, buffer ); // C4996  
   printf( "buffer: '%s' (%d chars)\n", buffer, strlen(buffer) );  
   value /= 10;  
   _gcvt( value, 12, buffer ); // C4996  
   printf( "buffer: '%s' (%d chars)\n", buffer, strlen(buffer) );  
}  
```  
  
 **The following numbers were converted by _gcvt(value,12,buffer):**  
**buffer: '-1234567890.12' (14 chars)**  
**buffer: '-12345678901.2' (14 chars)**  
**buffer: '-123456789012' (13 chars)**  
**buffer: '-1.23456789012e+012' (19 chars)**  
**buffer: '-12.3456789012' (14 chars)**  
**buffer: '-1.23456789012' (14 chars)**  
**buffer: '-0.123456789012' (15 chars)**  
**buffer: '-1.23456789012e-002' (19 chars)**   
## .NET Framework Equivalent  
 [System::Convert::ToString](https://msdn.microsoft.com/en-us/library/system.convert.tostring.aspx)  
  
## See Also  
 [Data Conversion](../vs140/Data-Conversion.md)   
 [Floating-Point Support](../vs140/Floating-Point-Support.md)   
 [atof, _atof_l, _wtof, _wtof_l](../vs140/atof--_atof_l--_wtof--_wtof_l.md)   
 [_ecvt](../vs140/_ecvt.md)   
 [_fcvt](../vs140/_fcvt.md)