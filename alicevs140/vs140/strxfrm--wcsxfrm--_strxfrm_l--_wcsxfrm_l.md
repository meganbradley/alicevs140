---
title: "strxfrm, wcsxfrm, _strxfrm_l, _wcsxfrm_l"
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
  - strxfrm
  - _wcsxfrm_l
  - _strxfrm_l
  - wcsxfrm
apilocation: 
  - msvcr120.dll
  - msvcrt.dll
  - msvcr90.dll
  - msvcr80.dll
  - msvcr110.dll
  - msvcr100.dll
  - msvcr110_clr0400.dll
apitype: DLLExport
ms.assetid: 6ba8e1f6-4484-49aa-83b8-bc2373187d9e
caps.latest.revision: 20
translation.priority.ht: 
  - de-de
  - ja-jp
---
# strxfrm, wcsxfrm, _strxfrm_l, _wcsxfrm_l
Transform a string based on locale-specific information.  
  
## Syntax  
  
```  
size_t strxfrm(  
   char *strDest,  
   const char *strSource,  
   size_t count   
);  
size_t wcsxfrm(  
   wchar_t *strDest,  
   const wchar_t *strSource,  
   size_t count   
);  
size_t _strxfrm_l(  
   char *strDest,  
   const char *strSource,  
   size_t count,  
   _locale_t locale  
);  
size_t wcsxfrm_l(  
   wchar_t *strDest,  
   const wchar_t *strSource,  
   size_t count,  
   _locale_t locale  
);  
```  
  
#### Parameters  
 `strDest`  
 Destination string.  
  
 `strSource`  
 Source string.  
  
 `count`  
 Maximum number of characters to place in `strDest`*.*  
  
 `locale`  
 The locale to use.  
  
## Return Value  
 Returns the length of the transformed string, not counting the terminating null character. If the return value is greater than or equal to `count`, the content of `strDest` is unpredictable. On an error, each function sets `errno` and returns `INT_MAX`. For an invalid character, `errno` is set to `EILSEQ`.  
  
## Remarks  
 The `strxfrm` function transforms the string pointed to by `strSource` into a new collated form that is stored in `strDest`. No more than `count` characters, including the null character, are transformed and placed into the resulting string. The transformation is made using the locale's `LC_COLLATE` category setting. For more information on `LC_COLLATE`, see [setlocale](../vs140/setlocale--_wsetlocale.md). `strxfrm` uses the current locale for its locale-dependent behavior; `_strxfrm_l` is identical except that it uses the locale passed in instead of the current locale. For more information, see [Locale](../vs140/Locale.md).  
  
 After the transformation, a call to `strcmp` with the two transformed strings yields results identical to those of a call to `strcoll` applied to the original two strings. As with `strcoll` and `stricoll`, `strxfrm` automatically handles multibyte-character strings as appropriate.  
  
 `wcsxfrm` is a wide-character version of `strxfrm`; the string arguments of `wcsxfrm` are wide-character pointers. For `wcsxfrm`, after the string transformation, a call to `wcscmp` with the two transformed strings yields results identical to those of a call to `wcscoll` applied to the original two strings. `wcsxfrm` and `strxfrm` behave identically otherwise. `wcsxfrm` uses the current locale for its locale-dependent behavior; `_wcsxfrm_l` uses the locale passed in instead of the current locale.  
  
 These functions validate their parameters. If `strSource` is a null pointer, or `strDest` is a NULL pointer (unless count is zero), or if `count` is greater than `INT_MAX`, the invalid parameter handler is invoked, as described in [Parameter Validation](../vs140/Parameter-Validation.md) . If execution is allowed to continue, these functions set `errno` to `EINVAL` and return `INT_MAX`.  
  
### Generic-Text Routine Mappings  
  
|TCHAR.H routine|_UNICODE & _MBCS not defined|_MBCS defined|_UNICODE defined|  
|---------------------|------------------------------------|--------------------|-----------------------|  
|`_tcsxfrm`|`strxfrm`|`strxfrm`|`wcsxfrm`|  
|`_tcsxfrm_l`|`_strxfrm_l`|`_strxfrm_l`|`_wcsxfrm_l`|  
  
 In the "C" locale, the order of the characters in the character set (ASCII character set) is the same as the lexicographic order of the characters. However, in other locales, the order of characters in the character set may differ from the lexicographic character order. For example, in certain European locales, the character 'a' (value 0x61) precedes the character '&\#x00E4;' (value 0xE4) in the character set, but the character 'ä' precedes the character 'a' lexicographically.  
  
 In locales for which the character set and the lexicographic character order differ, use `strxfrm` on the original strings and then `strcmp` on the resulting strings to produce a lexicographic string comparison according to the current locale's `LC_COLLATE` category setting. Thus, to compare two strings lexicographically in the above locale, use `strxfrm` on the original strings, then `strcmp` on the resulting strings. Alternately, you can use `strcoll` rather than `strcmp` on the original strings.  
  
 `strxfrm` is basically a wrapper around [LCMapString](http://msdn.microsoft.com/library/windows/desktop/dd318700) with `LCMAP_SORTKEY`.  
  
 The value of the following expression is the size of the array needed to hold the `strxfrm` transformation of the source string:  
  
```  
1 + strxfrm( NULL, string, 0 )  
```  
  
 In the "C" locale only, `strxfrm` is equivalent to the following:  
  
```  
strncpy( _string1, _string2, _count );  
return( strlen( _string1 ) );  
```  
  
## Requirements  
  
|Routine|Required header|  
|-------------|---------------------|  
|`strxfrm`|<string.h>|  
|`wcsxfrm`|<string.h> or <wchar.h>|  
|`_strxfrm_l`|<string.h>|  
|`_wcsxfrm_l`|<string.h> or <wchar.h>|  
  
 For additional compatibility information, see [Compatibility](../vs140/Compatibility.md) in the Introduction.  
  
## .NET Framework Equivalent  
 Not applicable. To call the standard C function, use `PInvoke`. For more information, see [Platform Invoke Examples](assetId:///15926806-f0b7-487e-93a6-4e9367ec689f).  
  
## See Also  
 [Data Conversion](../vs140/Data-Conversion.md)   
 [localeconv](../vs140/localeconv.md)   
 [setlocale, _wsetlocale](../vs140/setlocale--_wsetlocale.md)   
 [Locale](../vs140/Locale.md)   
 [String Manipulation](../vs140/String-Manipulation--CRT-.md)   
 [strcoll Functions](../vs140/strcoll-Functions.md)   
 [strcmp, wcscmp, _mbscmp](../vs140/strcmp--wcscmp--_mbscmp.md)   
 [strncmp, wcsncmp, _mbsncmp, _mbsncmp_l](../vs140/strncmp--wcsncmp--_mbsncmp--_mbsncmp_l.md)