---
title: "_strspnp, _wcsspnp, _mbsspnp, _mbsspnp_l"
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
  - _mbsspnp
  - _wcsspnp
  - _mbsspnp_l
  - _strspnp
apilocation: 
  - msvcrt.dll
  - msvcr100.dll
  - msvcr110_clr0400.dll
  - msvcr90.dll
  - msvcr110.dll
  - msvcr120.dll
  - msvcr80.dll
apitype: DLLExport
ms.assetid: 1ce18100-2edd-4c3b-af8b-53f204d80233
caps.latest.revision: 25
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _strspnp, _wcsspnp, _mbsspnp, _mbsspnp_l
Returns a pointer to the first character in a given string that is not in another given string.  
  
> [!IMPORTANT]
>  `_mbsspnp` and `_mbsspnp_l` cannot be used in applications that execute in the Windows Runtime. For more information, see [CRT functions not supported with /ZW](http://msdn.microsoft.com/library/windows/apps/jj606124.aspx).  
  
## Syntax  
  
```  
char *_strspnp(  
   const char *str,  
   const char *charset  
);  
wchar_t *_wcsspnp(  
   const unsigned wchar_t *str,  
   const unsigned wchar_t *charset  
);  
unsigned char *_mbsspnp(  
   const unsigned char *str,  
   const unsigned char *charset  
);  
unsigned char *_mbsspnp_l(  
   const unsigned char *str,  
   const unsigned char *charset,  
   _locale_t locale  
);  
  
```  
  
#### Parameters  
 `str`  
 Null-terminated string to search.  
  
 `charset`  
 Null-terminated character set.  
  
 `locale`  
 Locale to use.  
  
## Return Value  
 `_strspnp`, `_wcsspnp`, and `_mbsspnp` return a pointer to the first character in `str` that does not belong to the set of characters in `charset`*.* Each of these functions returns `NULL` if `str` consists entirely of characters from `charset`*.* For each of these routines, no return value is reserved to indicate an error.  
  
## Remarks  
 The `_mbsspnp` function returns a pointer to the multibyte character that is the first character in `str` that does not belong to the set of characters in `charset`. `_mbsspnp` recognizes multibyte-character sequences according to the [multibyte code page](../vs140/Code-Pages.md) currently in use. The search does not include terminating null characters.  
  
 If either `str` or `charset` is a null pointer, this function invokes the invalid parameter handler, as described in [Parameter Validation](../vs140/Parameter-Validation.md). If execution is allowed to continue, the function returns `NULL` and sets `errno` to `EINVAL`.  
  
### Generic-Text Routine Mappings  
  
|Tchar.h routine|_UNICODE and _MBCS not defined|_MBCS defined|_UNICODE defined|  
|---------------------|--------------------------------------|--------------------|-----------------------|  
|`_tcsspnp`|`_strspnp`|`_mbsspnp`|`_wcsspnp`|  
  
 `_strspnp` and `_wcsspnp` are single-byte character and wide-character versions of `_mbsspnp`. `_strspnp` and `_wcsspnp` behave identically to `_mbsspnp` otherwise; they are provided only for this mapping and should not be used for any other reason. For more information, see [Using Generic-Text Mappings](../vs140/Using-Generic-Text-Mappings.md) and [Generic-Text Mappings](../vs140/Generic-Text-Mappings.md).  
  
 `_mbsspnp_l` is identical except that it uses the locale parameter passed in instead. For more information, see [Locale](../vs140/Locale.md).  
  
## Requirements  
  
|Routine|Required header|  
|-------------|---------------------|  
|`_mbsspnp`|<mbstring.h>|  
|`_strspnp`|<tchar.h>|  
|`_wcsspnp`|<tchar.h>|  
  
 For more compatibility information, see [Compatibility](../vs140/Compatibility.md).  
  
## Example  
  
```  
// crt_mbsspnp.c  
#include <mbstring.h>  
#include <stdio.h>  
  
int main( void ) {  
   const unsigned char string1[] = "cabbage";  
   const unsigned char string2[] = "c";  
   unsigned char *ptr = 0;  
   ptr = _mbsspnp( string1, string2 );  
   printf( "%s\n", ptr);  
}  
```  
  
## Output  
  
```  
abbage  
```  
  
## .NET Framework Equivalent  
 Not applicable. To call the standard C function, use `PInvoke`. For more information, see [Platform Invoke Examples](assetId:///15926806-f0b7-487e-93a6-4e9367ec689f).  
  
## See Also  
 [String Manipulation](../vs140/String-Manipulation--CRT-.md)   
 [Locale](../vs140/Locale.md)   
 [Interpretation of Multibyte-Character Sequences](../vs140/Interpretation-of-Multibyte-Character-Sequences.md)   
 [strspn, wcsspn, _mbsspn, _mbsspn_l](../vs140/strspn--wcsspn--_mbsspn--_mbsspn_l.md)   
 [strncat_s, _strncat_s_l, wcsncat_s, _wcsncat_s_l, _mbsncat_s, _mbsncat_s_l](../vs140/strncat_s--_strncat_s_l--wcsncat_s--_wcsncat_s_l--_mbsncat_s--_mbsncat_s_l.md)   
 [strncmp, wcsncmp, _mbsncmp, _mbsncmp_l](../vs140/strncmp--wcsncmp--_mbsncmp--_mbsncmp_l.md)   
 [strncpy_s, _strncpy_s_l, wcsncpy_s, _wcsncpy_s_l, _mbsncpy_s, _mbsncpy_s_l](../vs140/strncpy_s--_strncpy_s_l--wcsncpy_s--_wcsncpy_s_l--_mbsncpy_s--_mbsncpy_s_l.md)   
 [_strnicmp, _wcsnicmp, _mbsnicmp, _strnicmp_l, _wcsnicmp_l, _mbsnicmp_l](../vs140/_strnicmp--_wcsnicmp--_mbsnicmp--_strnicmp_l--_wcsnicmp_l--_mbsnicmp_l.md)   
 [strrchr, wcsrchr, _mbsrchr, _mbsrchr_l](../vs140/strrchr--wcsrchr--_mbsrchr--_mbsrchr_l.md)