---
title: "_strlwr_s, _strlwr_s_l, _mbslwr_s, _mbslwr_s_l, _wcslwr_s, _wcslwr_s_l"
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
  - _strlwr_s_l
  - _mbslwr_s_l
  - _mbslwr_s
  - _wcslwr_s
  - _strlwr_s
  - _wcslwr_s_l
apilocation: 
  - msvcr90.dll
  - msvcrt.dll
  - msvcr120.dll
  - msvcr110_clr0400.dll
  - msvcr80.dll
  - msvcr100.dll
  - msvcr110.dll
apitype: DLLExport
ms.assetid: 4883d31b-bdac-4049-83a1-91dfdeceee79
caps.latest.revision: 42
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _strlwr_s, _strlwr_s_l, _mbslwr_s, _mbslwr_s_l, _wcslwr_s, _wcslwr_s_l
Converts a string to lowercase, by using the current locale or a locale object that's passed in. These versions of [_strlwr, _wcslwr](../vs140/_strlwr--_wcslwr--_mbslwr--_strlwr_l--_wcslwr_l--_mbslwr_l.md) have security enhancements, as described in [Security Enhancements in the CRT](../vs140/Security-Features-in-the-CRT.md).  
  
> [!IMPORTANT]
>  `_mbslwr_s` and `_mbslwr_s_l` cannot be used in applications that execute in the Windows Runtime. For more information, see [CRT functions not supported with /ZW](http://msdn.microsoft.com/library/windows/apps/jj606124.aspx).  
  
## Syntax  
  
```  
errno_t _strlwr_s(  
   char *str,  
   size_t numberOfElements  
);  
errno_t _strlwr_s_l(  
   char *str,  
   size_t numberOfElements,  
   _locale_t locale  
);  
errno_t _mbslwr_s(  
   unsigned char *str,  
   size_t numberOfElements  
);  
errno_t _mbslwr_s_l(  
   unsigned char *str,  
   size_t numberOfElements,  
   _locale_t locale  
);  
errno_t _wcslwr_s(  
   wchar_t *str,  
   size_t numberOfElements  
);  
errno_t _wcslwr_s_l(  
   wchar_t *str,  
   size_t numberOfElements,  
   _locale_t locale  
);  
template <size_t size>  
errno_t _strlwr_s(  
   char (&str)[size]  
); // C++ only  
template <size_t size>  
errno_t _strlwr_s_l(  
   char (&str)[size],  
   _locale_t locale  
); // C++ only  
template <size_t size>  
errno_t _mbslwr_s(  
   unsigned char (&str)[size]  
); // C++ only  
template <size_t size>  
errno_t _mbslwr_s_l(  
   unsigned char (&str)[size],  
   _locale_t locale  
); // C++ only  
template <size_t size>  
errno_t _wcslwr_s(  
   wchar_t (&str)[size]  
); // C++ only  
template <size_t size>  
errno_t _wcslwr_s_l(  
   wchar_t (&str)[size],  
   _locale_t locale  
); // C++ only  
```  
  
#### Parameters  
 `str`  
 Null-terminated string to convert to lowercase.  
  
 `numberOfElements`  
 Size of the buffer.  
  
 `locale`  
 The locale to use.  
  
## Return Value  
 Zero if successful; a non-zero error code on failure.  
  
 These functions validate their parameters. If `str` is not a valid null-terminated string, the invalid parameter handler is invoked, as described in [Parameter Validation](../vs140/Parameter-Validation.md) . If execution is allowed to continue, the functions return `EINVAL` and set `errno` to `EINVAL`. If `numberOfElements` is less than the length of the string, the functions also return `EINVAL` and set `errno` to `EINVAL`.  
  
## Remarks  
 The `_strlwr_s` function converts, in place, any uppercase letters in `str` to lowercase. `_mbslwr_s` is a multi-byte character version of `_strlwr_s`.`_wcslwr_s` is a wide-character version of `_strlwr_s`.  
  
 The output value is affected by the setting of the `LC_CTYPE` category setting of the locale; see [setlocale](../vs140/setlocale--_wsetlocale.md) for more information. The versions of these functions without the `_l` suffix use the current locale for this locale-dependent behavior; the versions with the `_l` suffix are identical except that they use the locale parameter passed in instead. For more information, see [Locale](../vs140/Locale.md).  
  
 In C++, using these functions is simplified by template overloads; the overloads can infer buffer length automatically (eliminating the need to specify a size argument) and they can automatically replace older, non-secure functions with their newer, secure counterparts. For more information, see [Secure Template Overloads](../vs140/Secure-Template-Overloads.md).  
  
 The debug versions of these functions first fill the buffer with 0xFD. To disable this behavior, use [_CrtSetDebugFillThreshold](../vs140/_CrtSetDebugFillThreshold.md).  
  
### Generic-Text Routine Mappings  
  
|TCHAR.H routine|_UNICODE & _MBCS not defined|_MBCS defined|_UNICODE defined|  
|---------------------|------------------------------------|--------------------|-----------------------|  
|`_tcslwr_s`|`_strlwr_s`|`_mbslwr_s`|`_wcslwr_s`|  
|`_tcslwr_s_l`|`_strlwr_s_l`|`_mbslwr_s_l`|`_wcslwr_s_l`|  
  
## Requirements  
  
|Routine|Required header|  
|-------------|---------------------|  
|`_strlwr_s`, `_strlwr_s_l`|<string.h>|  
|`_mbslwr_s`, `_mbslwr_s_l`|<mbstring.h>|  
|`_wcslwr_s`, `_wcslwr_s_l`|<string.h> or <wchar.h>|  
  
 For additional compatibility information, see [Compatibility](../vs140/Compatibility.md).  
  
## Example  
  
```  
// crt_strlwr_s.cpp  
// This program uses _strlwr_s and _strupr_s to create  
// uppercase and lowercase copies of a mixed-case string.  
//  
  
#include <string.h>  
#include <stdio.h>  
#include <stdlib.h>  
  
int main()  
{  
   char str[] = "The String to End All Strings!";  
   char *copy1, *copy2;  
   errno_t err;  
  
   err = _strlwr_s( copy1 = _strdup(str), strlen(str) + 1);  
   err = _strupr_s( copy2 = _strdup(str), strlen(str) + 1);  
  
   printf( "Mixed: %s\n", str );  
   printf( "Lower: %s\n", copy1 );  
   printf( "Upper: %s\n", copy2 );  
  
   free( copy1 );  
   free( copy2 );  
  
   return 0;  
}  
```  
  
 **Mixed: The String to End All Strings!**  
**Lower: the string to end all strings!**  
**Upper: THE STRING TO END ALL STRINGS!**   
## .NET Framework Equivalent  
 [System::String::ToLower](https://msdn.microsoft.com/en-us/library/system.string.tolower.aspx)  
  
## See Also  
 [String Manipulation](../vs140/String-Manipulation--CRT-.md)   
 [Locale](../vs140/Locale.md)   
 [Interpretation of Multibyte-Character Sequences](../vs140/Interpretation-of-Multibyte-Character-Sequences.md)   
 [_strupr_s, _strupr_s_l, _mbsupr_s, _mbsupr_s_l, _wcsupr_s, _wcsupr_s_l](../vs140/_strupr_s--_strupr_s_l--_mbsupr_s--_mbsupr_s_l--_wcsupr_s--_wcsupr_s_l.md)