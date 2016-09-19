---
title: "_strtoi64, _wcstoi64, _strtoi64_l, _wcstoi64_l"
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
  - _strtoi64
  - _strtoi64_l
  - _wcstoi64_l
  - _wcstoi64
apilocation: 
  - msvcr100.dll
  - msvcr120.dll
  - msvcr110_clr0400.dll
  - msvcrt.dll
  - msvcr110.dll
  - msvcr80.dll
  - msvcr90.dll
apitype: DLLExport
ms.assetid: ea2abc50-7bfe-420e-a46b-703c3153593a
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _strtoi64, _wcstoi64, _strtoi64_l, _wcstoi64_l
Convert a string to an `__int64` value.  
  
## Syntax  
  
```  
__int64 _strtoi64(  
   const char *nptr,  
   char **endptr,  
   int base   
);  
__int64 _wcstoi64(  
   const wchar_t *nptr,  
   wchar_t **endptr,  
   int base   
);  
__int64 _strtoi64_l(  
   const char *nptr,  
   char **endptr,  
   int base,  
   _locale_t locale  
);  
__int64 _wcstoi64_l(  
   const wchar_t *nptr,  
   wchar_t **endptr,  
   int base,  
   _locale_t locale  
);  
```  
  
#### Parameters  
 `nptr`  
 Null-terminated string to convert.  
  
 `endptr`  
 Pointer to character that stops scan.  
  
 `base`  
 Number base to use.  
  
 `locale`  
 The locale to use.  
  
## Return Value  
 `_strtoi64` returns the value represented in the string `nptr`, except when the representation would cause an overflow, in which case it returns `_I64_MAX` or `_I64_MIN`. The function will return 0 if no conversion can be performed. `_wcstoi64` returns values analogously to `strtoi64`.  
  
 `_I64_MAX` and `_I64_MIN` are defined in LIMITS.H.  
  
 If `nptr` is `NULL` or the `base` is nonzero and either less than 2 or greater than 36, `errno` is set to `EINVAL`.  
  
 See [_doserrno, errno, _sys_errlist, and _sys_nerr](../vs140/errno--_doserrno--_sys_errlist--and-_sys_nerr.md) for more information on these, and other, return codes.  
  
## Remarks  
 The `_strtoi64`function converts `nptr` to an `__int64`. Both functions stop reading the string `nptr` at the first character they cannot recognize as part of a number. This may be the terminating null character, or it may be the first numeric character greater than or equal to `base`. `_wcstoi64` is a wide-character version of `_strtoi64`; its `nptr` argument is a wide-character string. These functions behave identically otherwise.  
  
### Generic-Text Routine Mappings  
  
|TCHAR.H routine|_UNICODE & _MBCS not defined|_MBCS defined|_UNICODE defined|  
|---------------------|------------------------------------|--------------------|-----------------------|  
|`_tcstoi64`|`_strtoi64`|`_strtoi64`|`_wcstoi64`|  
|`_tcstoi64_l`|`_strtoi64_l`|`_strtoi64_l`|`_wcstoi64_l`|  
  
 The locale's `LC_NUMERIC` category setting determines recognition of the radix character in `nptr`*;* for more information, see [setlocale](../vs140/setlocale--_wsetlocale.md). The functions without the _l suffix use the current locale; `_strtoi64_l` and`_wcstoi64_l` are identical to the corresponding function without the `_l` suffix except that they use the locale passed in instead. For more information, see [Locale](../vs140/Locale.md).  
  
 If `endptr` is not `NULL`, a pointer to the character that stopped the scan is stored at the location pointed to by `endptr`. If no conversion can be performed (no valid digits were found or an invalid base was specified), the value of `nptr` is stored at the location pointed to by `endptr`.  
  
 `_strtoi64` expects `nptr` to point to a string of the following form:  
  
 [`whitespace`] [{`+` &#124; `–`}] [`0` [{ `x` &#124; `X` }]] [`digits`]  
  
 A `whitespace` may consist of space and tab characters, which are ignored; `digits` are one or more decimal digits. The first character that does not fit this form stops the scan. If `base` is between 2 and 36, then it is used as the base of the number. If `base` is 0, the initial characters of the string pointed to by `nptr` are used to determine the base. If the first character is 0 and the second character is not 'x' or 'X', the string is interpreted as an octal integer. If the first character is '0' and the second character is 'x' or 'X', the string is interpreted as a hexadecimal integer. If the first character is '1' through '9', the string is interpreted as a decimal integer. The letters 'a' through 'z' (or 'A' through 'Z') are assigned the values 10 through 35; only letters whose assigned values are less than `base` are permitted. The first character outside the range of the base stops the scan. For example, if `base` is 0 and the first character scanned is '0', an octal integer is assumed and an '8' or '9' character will stop the scan.  
  
## Requirements  
  
|Routine|Required header|  
|-------------|---------------------|  
|`_strtoi64`, `_strtoi64_l`|<stdlib.h>|  
|`_wcstoi64`, `_wcstoi64_l`|<stdlib.h> or <wchar.h>|  
  
 For additional compatibility information, see [Compatibility](../vs140/Compatibility.md) in the Introduction.  
  
## See Also  
 [Data Conversion](../vs140/Data-Conversion.md)   
 [Locale](../vs140/Locale.md)   
 [localeconv](../vs140/localeconv.md)   
 [setlocale, _wsetlocale](../vs140/setlocale--_wsetlocale.md)   
 [String to Numeric Value Functions](../vs140/String-to-Numeric-Value-Functions.md)   
 [strtod, _strtod_l, wcstod](../vs140/strtod--_strtod_l--wcstod--_wcstod_l.md)   
 [strtoul, _strtoul_l, wcstoul, _wcstoul_l](../vs140/strtoul--_strtoul_l--wcstoul--_wcstoul_l.md)   
 [atof, _atof_l, _wtof, _wtof_l](../vs140/atof--_atof_l--_wtof--_wtof_l.md)