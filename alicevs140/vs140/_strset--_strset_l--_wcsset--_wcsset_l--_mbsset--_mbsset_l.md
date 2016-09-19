---
title: "_strset, _strset_l, _wcsset, _wcsset_l, _mbsset, _mbsset_l"
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
  - _wcsset
  - _mbsset
  - _strset_l
  - _strset
  - _wcsset_l
  - _mbsset_l
apilocation: 
  - msvcr100.dll
  - msvcrt.dll
  - msvcr110_clr0400.dll
  - msvcr110.dll
  - msvcr120.dll
  - msvcr80.dll
  - msvcr90.dll
apitype: DLLExport
ms.assetid: c42ded42-2ed9-4f06-a0a9-247ba305473a
caps.latest.revision: 31
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _strset, _strset_l, _wcsset, _wcsset_l, _mbsset, _mbsset_l
Sets characters of a string to a character. More secure versions of these functions are available; see [_strset_s, _strset_s_l, _wcsset_s, _wcsset_s_l, _mbsset_s, _mbsset_s_l](../vs140/_strset_s--_strset_s_l--_wcsset_s--_wcsset_s_l--_mbsset_s--_mbsset_s_l.md).  
  
> [!IMPORTANT]
>  `_mbsset` and `_mbsset_l` cannot be used in applications that execute in the [!INCLUDE[wrt](../vs140/includes/wrt_md.md)]. For more information, see [CRT functions not supported with /ZW](http://msdn.microsoft.com/library/windows/apps/jj606124.aspx).  
  
## Syntax  
  
```  
char *_strset(  
   char *str,  
   int c   
);  
char *_strset_l(  
   char *str,  
   int c,  
   locale_t locale  
);  
wchar_t *_wcsset(  
   wchar_t *str,  
   wchar_t c   
);  
wchar_t *_wcsset_l(  
   wchar_t *str,  
   wchar_t c,  
   locale_t locale  
);  
unsigned char *_mbsset(  
   unsigned char *str,  
   unsigned int c   
);  
unsigned char *_mbsset_l(  
   unsigned char *str,  
   unsigned int c,  
   _locale_t locale  
);  
```  
  
#### Parameters  
 `str`  
 Null-terminated string to be set.  
  
 `c`  
 Character setting.  
  
 `locale`  
 Locale to use.  
  
## Return Value  
 Returns a pointer to the altered string.  
  
## Remarks  
 The `_strset` function sets all characters (except the terminating null character) of `str` to `c`, converted to `char`. `_wcsset` and `_mbsset_l` are wide-character and multibyte-character versions of `_strset`, and the data types of the arguments and return values vary accordingly. These functions behave identically otherwise.  
  
 `_mbsset` validates its parameters. If `str` is a null pointer, the invalid parameter handler is invoked, as described in [Parameter Validation](../vs140/Parameter-Validation.md). If execution is allowed to continue,`_mbsset` returns `NULL` and sets `errno` to `EINVAL`. `_strset` and `_wcsset` do not validate their parameters.  
  
 The output value is affected by the setting of the `LC_CTYPE` category setting of the locale; see [setlocale, _wsetlocale](../vs140/setlocale--_wsetlocale.md) for more information. The versions of these functions are identical, except that the ones that don't have the `_l` suffix use the current locale and the ones that do have the `_l` suffix instead use the locale parameter that's passed in. For more information, see [Locale](../vs140/Locale.md).  
  
> [!IMPORTANT]
>  These functions might be vulnerable to buffer overrun threats. Buffer overruns can be used for system attacks because they can cause an unwarranted elevation of privilege. For more information, see [Avoiding Buffer Overruns](http://msdn.microsoft.com/library/windows/desktop/ms717795).  
  
### Generic-Text Routine Mappings  
  
|TCHAR.H routine|_UNICODE & _MBCS not defined|_MBCS defined|_UNICODE defined|  
|---------------------|------------------------------------|--------------------|-----------------------|  
|`_tcsset`|`_strset`|`_mbsset`|`_wcsset`|  
|`_tcsset_l`|`_strset_l`|`_mbsset_l`|`_wcsset_l`|  
  
## Requirements  
  
|Routine|Required header|  
|-------------|---------------------|  
|`_strset`|<string.h>|  
|`_strset_l`|<tchar.h>|  
|`_wcsset`|<string.h> or <wchar.h>|  
|`_wcsset_l`|<tchar.h>|  
|`_mbsset`, `_mbsset_l`|<mbstring.h>|  
  
 For additional compatibility information, see [Compatibility](../vs140/Compatibility.md).  
  
## Example  
  
```  
// crt_strset.c  
// compile with: /W3  
  
#include <string.h>  
#include <stdio.h>  
  
int main( void )  
{  
   char string[] = "Fill the string with something.";  
   printf( "Before: %s\n", string );  
   _strset( string, '*' ); // C4996  
   // Note: _strset is deprecated; consider using _strset_s instead  
   printf( "After:  %s\n", string );  
}  
```  
  
 **Before: Fill the string with something.**  
**After:  \*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\***   
## .NET Framework Equivalent  
 Not applicable. To call the standard C function, use `PInvoke`. For more information, see [Platform Invoke Examples](assetId:///15926806-f0b7-487e-93a6-4e9367ec689f).  
  
## See Also  
 [String Manipulation](../vs140/String-Manipulation--CRT-.md)   
 [Locale](../vs140/Locale.md)   
 [Interpretation of Multibyte-Character Sequences](../vs140/Interpretation-of-Multibyte-Character-Sequences.md)   
 [_mbsnbset, _mbsnbset_l](../vs140/_mbsnbset--_mbsnbset_l.md)   
 [memset, wmemset](../vs140/memset--wmemset.md)   
 [strcat, wcscat, _mbscat](../vs140/strcat--wcscat--_mbscat.md)   
 [strcmp, wcscmp, _mbscmp](../vs140/strcmp--wcscmp--_mbscmp.md)   
 [strcpy, wcscpy, _mbscpy](../vs140/strcpy--wcscpy--_mbscpy.md)   
 [_strnset, _wcsnset, _mbsnset, _mbsnset_l](../vs140/_strnset--_strnset_l--_wcsnset--_wcsnset_l--_mbsnset--_mbsnset_l.md)