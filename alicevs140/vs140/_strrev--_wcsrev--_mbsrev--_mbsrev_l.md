---
title: "_strrev, _wcsrev, _mbsrev, _mbsrev_l"
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
  - _wcsrev
  - _mbsrev
  - _strrev
  - _mbsrev_l
apilocation: 
  - msvcr100.dll
  - msvcr110_clr0400.dll
  - msvcr90.dll
  - msvcrt.dll
  - msvcr110.dll
  - msvcr120.dll
  - msvcr80.dll
apitype: DLLExport
ms.assetid: 87863e89-4fa0-421c-af48-25d8516fe72f
caps.latest.revision: 25
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _strrev, _wcsrev, _mbsrev, _mbsrev_l
Reverses the characters of a string.  
  
> [!IMPORTANT]
>  `_mbsrev` and `_mbsrev_l` cannot be used in applications that execute in the [!INCLUDE[wrt](../vs140/includes/wrt_md.md)]. For more information, see [CRT functions not supported with /ZW](http://msdn.microsoft.com/library/windows/apps/jj606124.aspx).  
  
## Syntax  
  
```  
char *_strrev(  
   char *str   
);  
wchar_t *_wcsrev(  
   wchar_t *str   
);  
unsigned char *_mbsrev(  
   unsigned char *str   
);  
unsigned char *_mbsrev_l(  
   unsigned char *str,  
   _locale_t locale   
);  
```  
  
#### Parameters  
 `str`  
 Null-terminated string to reverse.  
  
 `locale`  
 Locale to use.  
  
## Return Value  
 Returns a pointer to the altered string. No return value is reserved to indicate an error.  
  
## Remarks  
 The `_strrev` function reverses the order of the characters in `string`. The terminating null character remains in place. `_wcsrev` and `_mbsrev` are wide-character and multibyte-character versions of `_strrev`. The arguments and return value of `_wcsrev` are wide-character strings; those of `_mbsrev` are multibyte-character strings. For `_mbsrev`, the order of bytes in each multibyte character in `string` is not changed. These three functions behave identically otherwise.  
  
 `_mbsrev` validates its parameters. If either `string1` or `string2` is a null pointer, the invalid parameter handler is invoked, as described in [Parameter Validation](../vs140/Parameter-Validation.md). If execution is allowed to continue, `_mbsrev` returns `NULL` and sets `errno` to `EINVAL`. `_strrev` and `_wcsrev` do not validate their parameters.  
  
 The output value is affected by the setting of the `LC_CTYPE` category setting of the locale; see [setlocale, _wsetlocale](../vs140/setlocale--_wsetlocale.md) for more information. The versions of these functions are identical, except that the ones that don't have the `_l` suffix use the current locale and the ones that do have the`_l` suffix instead use the locale parameter that's passed in. For more information, see [Locale](../vs140/Locale.md).  
  
> [!IMPORTANT]
>  These functions might be vulnerable to buffer overrun threats. Buffer overruns can be used for system attacks because they can cause an unwarranted elevation of privilege. For more information, see [Avoiding Buffer Overruns](http://msdn.microsoft.com/library/windows/desktop/ms717795).  
  
### Generic-Text Routine Mappings  
  
|TCHAR.H routine|_UNICODE & _MBCS not defined|_MBCS defined|_UNICODE defined|  
|---------------------|------------------------------------|--------------------|-----------------------|  
|`_tcsrev`|`_strrev`|`_mbsrev`|`_wcsrev`|  
|**n/a**|**n/a**|`_mbsrev_l`|**n/a**|  
  
## Requirements  
  
|Routine|Required header|  
|-------------|---------------------|  
|`_strrev`|<string.h>|  
|`_wcsrev`|<string.h> or <wchar.h>|  
|`_mbsrev`, `_mbsrev_l`|<mbstring.h>|  
  
 For additional compatibility information, see [Compatibility](../vs140/Compatibility.md).  
  
## Example  
  
```  
// crt_strrev.c  
// This program checks a string to see  
// whether it is a palindrome: that is, whether  
// it reads the same forward and backward.  
//  
  
#include <string.h>  
#include <stdio.h>  
  
int main( void )  
{  
   char* string = "Able was I ere I saw Elba";  
   int result;  
  
   // Reverse string and compare (ignore case):  
   result = _stricmp( string, _strrev( _strdup( string ) ) );  
   if( result == 0 )  
      printf( "The string \"%s\" is a palindrome\n", string );  
   else  
      printf( "The string \"%s\" is not a palindrome\n", string );  
}  
```  
  
 **The string "Able was I ere I saw Elba" is a palindrome**   
## .NET Framework Equivalent  
 Not applicable. To call the standard C function, use `PInvoke`. For more information, see [Platform Invoke Examples](assetId:///15926806-f0b7-487e-93a6-4e9367ec689f).  
  
## See Also  
 [String Manipulation](../vs140/String-Manipulation--CRT-.md)   
 [Locale](../vs140/Locale.md)   
 [Interpretation of Multibyte-Character Sequences](../vs140/Interpretation-of-Multibyte-Character-Sequences.md)   
 [strcpy, wcscpy, _mbscpy](../vs140/strcpy--wcscpy--_mbscpy.md)   
 [_strset, _wcsset, _mbsset, _mbsset_l](../vs140/_strset--_strset_l--_wcsset--_wcsset_l--_mbsset--_mbsset_l.md)