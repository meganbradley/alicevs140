---
title: "strtoul, _strtoul_l, wcstoul, _wcstoul_l"
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
  - _wcstoul_l
  - _strtoul_l
  - strtoul
  - wcstoul
apilocation: 
  - msvcr90.dll
  - msvcr110.dll
  - msvcr80.dll
  - msvcr110_clr0400.dll
  - msvcr100.dll
  - msvcr120.dll
  - msvcrt.dll
apitype: DLLExport
ms.assetid: 38f2afe8-8178-4e0b-8bbe-d5c6ad66e3ab
caps.latest.revision: 23
translation.priority.ht: 
  - de-de
  - ja-jp
---
# strtoul, _strtoul_l, wcstoul, _wcstoul_l
Convert strings to an unsigned long-integer value.  
  
## Syntax  
  
```  
unsigned long strtoul(  
   const char *nptr,  
   char **endptr,  
   int base   
);  
unsigned long _strtoul_l(  
   const char *nptr,  
   char **endptr,  
   int base,  
   _locale_t locale  
);  
unsigned long wcstoul(  
   const wchar_t *nptr,  
   wchar_t **endptr,  
   int base   
);  
unsigned long _wcstoul_l(  
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
 Locale to use.  
  
## Return Value  
 `strtoul` returns the converted value, if any, or `ULONG_MAX` on overflow. `strtoul` returns 0 if no conversion can be performed. `wcstoul` returns values analogously to `strtoul`. For both functions, `errno` is set to `ERANGE` if overflow or underflow occurs.  
  
 See [_doserrno, errno, _sys_errlist, and _sys_nerr](../vs140/errno--_doserrno--_sys_errlist--and-_sys_nerr.md) for more information on this, and other, return codes.  
  
## Remarks  
 Each of these functions converts the input string `nptr` to an `unsigned` `long`.  
  
 `strtoul` stops reading the string `nptr` at the first character it cannot recognize as part of a number. This may be the terminating null character, or it may be the first numeric character greater than or equal to `base`. The `LC_NUMERIC` category setting of the locale determines recognition of the radix character in `nptr`; for more information, see [setlocale](../vs140/setlocale--_wsetlocale.md). `strtoul` and `wcstoul` use the current locale; `_strtoul_l` and `_wcstoul_l` are identical except that they use the locale passed in instead. For more information, see [Locale](../vs140/Locale.md).  
  
 If `endptr` is not `NULL`, a pointer to the character that stopped the scan is stored at the location pointed to by `endptr`. If no conversion can be performed (no valid digits were found or an invalid base was specified), the value of `nptr` is stored at the location pointed to by `endptr`.  
  
 `wcstoul` is a wide-character version of `strtoul`; its `nptr` argument is a wide-character string. Otherwise these functions behave identically.  
  
### Generic-Text Routine Mappings  
  
|TCHAR.H routine|_UNICODE & _MBCS not defined|_MBCS defined|_UNICODE defined|  
|---------------------|------------------------------------|--------------------|-----------------------|  
|`_tcstoul`|`strtoul`|`strtoul`|`wcstoul`|  
|`_tcstoul_l`|`strtoul_l`|`_strtoul_l`|`_wcstoul_l`|  
  
 `strtoul` expects `nptr` to point to a string of the following form:  
  
 [`whitespace`] [{`+` &#124; `–`}] [`0` [{ `x` &#124; `X` }]] [`digits`]  
  
 A `whitespace` may consist of space and tab characters, which are ignored; `digits` are one or more decimal digits. The first character that does not fit this form stops the scan. If `base` is between 2 and 36, then it is used as the base of the number. If `base` is 0, the initial characters of the string pointed to by `nptr` are used to determine the base. If the first character is 0 and the second character is not 'x' or 'X', the string is interpreted as an octal integer. If the first character is '0' and the second character is 'x' or 'X', the string is interpreted as a hexadecimal integer. If the first character is '1' through '9', the string is interpreted as a decimal integer. The letters 'a' through 'z' (or 'A' through 'Z') are assigned the values 10 through 35; only letters whose assigned values are less than `base` are permitted. The first character outside the range of the base stops the scan. For example, if `base` is 0 and the first character scanned is '0', an octal integer is assumed and an '8' or '9' character will stop the scan. `strtoul` allows a plus (`+`) or minus (`–`) sign prefix; a leading minus sign indicates that the return value is negated.  
  
## Requirements  
  
|Routine|Required header|  
|-------------|---------------------|  
|`strtoul`|<stdlib.h>|  
|`wcstoul`|<stdlib.h> or <wchar.h>|  
|`_strtoul_l`|<stdlib.h>|  
|`_wcstoul_l`|<stdlib.h> or <wchar.h>|  
  
 For additional compatibility information, see [Compatibility](../vs140/Compatibility.md) in the Introduction.  
  
## Example  
 See the example for [strtod](../vs140/strtod--_strtod_l--wcstod--_wcstod_l.md).  
  
## .NET Framework Equivalent  
 [System::Convert::ToUInt64](https://msdn.microsoft.com/en-us/library/system.convert.touint32.aspx)  
  
## See Also  
 [Data Conversion](../vs140/Data-Conversion.md)   
 [Locale](../vs140/Locale.md)   
 [localeconv](../vs140/localeconv.md)   
 [setlocale, _wsetlocale](../vs140/setlocale--_wsetlocale.md)   
 [String to Numeric Value Functions](../vs140/String-to-Numeric-Value-Functions.md)   
 [strtod, _strtod_l, wcstod](../vs140/strtod--_strtod_l--wcstod--_wcstod_l.md)   
 [strtol, wcstol, _strtol_l, _wcstol_l](../vs140/strtol--wcstol--_strtol_l--_wcstol_l.md)   
 [atof, _atof_l, _wtof, _wtof_l](../vs140/atof--_atof_l--_wtof--_wtof_l.md)