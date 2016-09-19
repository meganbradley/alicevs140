---
title: "atof, _atof_l, _wtof, _wtof_l"
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
  - _wtof_l
  - atof
  - _atof_l
  - _wtof
apilocation: 
  - msvcr90.dll
  - msvcr100.dll
  - msvcr110.dll
  - msvcrt.dll
  - msvcr80.dll
  - msvcr110_clr0400.dll
  - msvcr120.dll
apitype: DLLExport
ms.assetid: eb513241-c9a9-4f5c-b7e7-a49b14abfb75
caps.latest.revision: 24
translation.priority.ht: 
  - de-de
  - ja-jp
---
# atof, _atof_l, _wtof, _wtof_l
Convert a string to double.  
  
## Syntax  
  
```  
double atof(  
   const char *str   
);  
double _atof_l(  
   const char *str,  
   _locale_t locale  
);  
double _wtof(  
   const wchar_t *str   
);  
double _wtof_l(  
   const wchar_t *str,  
   _locale_t locale  
);  
```  
  
#### Parameters  
 `str`  
 String to be converted.  
  
 `locale`  
 Locale to use.  
  
## Return Value  
 Each function returns the `double` value produced by interpreting the input characters as a number. The return value is 0.0 if the input cannot be converted to a value of that type.  
  
 In all out-of-range cases, errno is set to `ERANGE`. If the parameter passed in is `NULL`, the invalid parameter handler is invoked, as described in [Parameter Validation](../vs140/Parameter-Validation.md). If execution is allowed to continue, these functions set `errno` to `EINVAL` and return 0.  
  
## Remarks  
 These functions convert a character string to a double-precision, floating-point value.  
  
 The input string is a sequence of characters that can be interpreted as a numerical value of the specified type. The function stops reading the input string at the first character that it cannot recognize as part of a number. This character may be the null character ('\0' or L'\0') terminating the string.  
  
 The `str` argument to `atof` and `_wtof` has the following form:  
  
 [`whitespace`] [`sign`] [`digits`] [`.digits`] [ {`d` &#124; `D` &#124; `e` &#124; `E` }[`sign`]`digits`]  
  
 A `whitespace` consists of space or tab characters, which are ignored; `sign` is either plus (+) or minus (–); and `digits` are one or more decimal digits. If no digits appear before the decimal point, at least one must appear after the decimal point. The decimal digits may be followed by an exponent, which consists of an introductory letter (`d`, `D`, `e`, or `E`) and an optionally signed decimal integer.  
  
 The versions of these functions with the `_l` suffix are identical except that they use the locale parameter passed in instead of the current locale.  
  
### Generic-Text Routine Mappings  
  
|TCHAR.H routine|_UNICODE & _MBCS not defined|_MBCS defined|_UNICODE defined|  
|---------------------|------------------------------------|--------------------|-----------------------|  
|`_tstof`|`atof`|`atof`|`_wtof`|  
|`_ttof`|`atof`|`atof`|`_wtof`|  
  
## Requirements  
  
|Routine(s)|Required header|  
|------------------|---------------------|  
|`atof`|<math.h> and <stdlib.h>|  
|`_atof_l`|<math.h> and <stdlib.h>|  
|`_wtof`, `_wtof_l`|<stdlib.h> or <wchar.h>|  
  
## Example  
 This program shows how numbers stored as strings can be converted to numeric values using the `atof` function.  
  
```  
// crt_atof.c  
//  
// This program shows how numbers stored as   
// strings can be converted to numeric  
// values using the atof function.  
  
#include <stdlib.h>  
#include <stdio.h>  
  
int main( void )  
{  
    char    *str = NULL;  
    double  value = 0;  
  
    // An example of the atof function  
    // using leading and training spaces.  
    str = "  3336402735171707160320 ";  
    value = atof( str );  
    printf( "Function: atof( \"%s\" ) = %e\n", str, value );  
  
    // Another example of the atof function  
    // using the 'd' exponential formatting keyword.  
    str = "3.1412764583d210";  
    value = atof( str );  
    printf( "Function: atof( \"%s\" ) = %e\n", str, value );  
  
    // An example of the atof function  
    // using the 'e' exponential formatting keyword.  
    str = "  -2309.12E-15";  
    value = atof( str );  
    printf( "Function: atof( \"%s\" ) = %e\n", str, value );  
  
}  
```  
  
 **Function: atof( "  3336402735171707160320 " ) = 3.336403e+021**  
**Function: atof( "3.1412764583d210" ) = 3.141276e+210**  
**Function: atof( "  -2309.12E-15" ) = -2.309120e-012**   
## .NET Framework Equivalent  
  
-   [System::Convert::ToSingle](https://msdn.microsoft.com/en-us/library/system.convert.tosingle.aspx)  
  
-   [System::Convert::ToDouble](https://msdn.microsoft.com/en-us/library/system.convert.todouble.aspx)  
  
## See Also  
 [Data Conversion](../vs140/Data-Conversion.md)   
 [Floating-Point Support](../vs140/Floating-Point-Support.md)   
 [Locale](../vs140/Locale.md)   
 [_ecvt](../vs140/_ecvt.md)   
 [_fcvt](../vs140/_fcvt.md)   
 [_gcvt](../vs140/_gcvt.md)   
 [setlocale, _wsetlocale](../vs140/setlocale--_wsetlocale.md)   
 [_atodbl, _atoldbl, _atoflt](../vs140/_atodbl--_atodbl_l--_atoldbl--_atoldbl_l--_atoflt--_atoflt_l.md)