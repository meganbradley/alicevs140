---
title: "strlen, wcslen, _mbslen, _mbslen_l, _mbstrlen, _mbstrlen_l"
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
  - _mbslen
  - _mbslen_l
  - _mbstrlen
  - wcslen
  - _mbstrlen_l
  - strlen
apilocation: 
  - msvcr110_clr0400.dll
  - msvcr100.dll
  - msvcrt.dll
  - msvcr120.dll
  - msvcr80.dll
  - msvcr90.dll
  - msvcr110.dll
  - msvcr120_clr0400.dll
apitype: DLLExport
ms.assetid: 16462f2a-1e0f-4eb3-be55-bf1c83f374c2
caps.latest.revision: 32
translation.priority.ht: 
  - de-de
  - ja-jp
---
# strlen, wcslen, _mbslen, _mbslen_l, _mbstrlen, _mbstrlen_l
Gets the length of a string, by using the current locale or a specified locale. More secure versions of these functions are available; see [strnlen, wcsnlen, _mbsnlen, _mbsnlen_l, _mbstrnlen, _mbstrnlen_l](../vs140/strnlen--strnlen_s--wcsnlen--wcsnlen_s--_mbsnlen--_mbsnlen_l--_mbstrnlen--_mbstrnlen_l.md)  
  
> [!IMPORTANT]
>  `_mbslen`, `_mbslen_l`, `_mbstrlen`, and `_mbstrlen_l` cannot be used in applications that execute in the Windows Runtime. For more information, see [CRT functions not supported with /ZW](http://msdn.microsoft.com/library/windows/apps/jj606124.aspx).  
  
## Syntax  
  
```  
size_t strlen(  
   const char *str  
);  
size_t wcslen(  
   const wchar_t *str   
);  
size_t _mbslen(  
   const unsigned char *str   
);  
size_t _mbslen_l(  
   const unsigned char *str,  
   _locale_t locale  
);  
size_t _mbstrlen(  
   const char *str  
);  
size_t _mbstrlen_l(  
   const char *str,  
   _locale_t locale  
);  
```  
  
#### Parameters  
 `str`  
 Null-terminated string.  
  
 `locale`  
 Locale to use.  
  
## Return Value  
 Each of these functions returns the number of characters in `str`, excluding the terminal `NULL`. No return value is reserved to indicate an error, except for `_mbstrlen` and `_mbstrlen_l`, which return `((size_t)(-1))` if the string contains an invalid multibyte character.  
  
## Remarks  
 `strlen` interprets the string as a single-byte character string, so its return value is always equal to the number of bytes, even if the string contains multibyte characters. `wcslen` is a wide-character version of `strlen`; the argument of `wcslen` is a wide-character string and the count of characters is in wide (two-byte) characters. `wcslen` and `strlen` behave identically otherwise.  
  
 **Security Note** These functions incur a potential threat brought about by a buffer overrun problem. Buffer overrun problems are a frequent method of system attack, resulting in an unwarranted elevation of privilege. For more information, see [Avoiding Buffer Overruns](http://msdn.microsoft.com/library/windows/desktop/ms717795).  
  
### Generic-Text Routine Mappings  
  
|TCHAR.H routine|_UNICODE & _MBCS not defined|_MBCS defined|_UNICODE defined|  
|---------------------|------------------------------------|--------------------|-----------------------|  
|`_tcslen`|`strlen`|`strlen`|`wcslen`|  
|`_tcsclen`|`strlen`|`_mbslen`|`wcslen`|  
|`_tcsclen_l`|`strlen`|`_mbslen_l`|`wcslen`|  
  
 `_mbslen` and `_mbslen_l` return the number of multibyte characters in a multibyte-character string but they do not test for multibyte-character validity. `_mbstrlen` and `_mbstrlen_l` test for multibyte-character validity and recognize multibyte-character sequences. If the string passed to `_mbstrlen` or `_mbstrlen_l` contains an invalid multibyte character for the code page, the function returns -1 and sets `errno` to `EILSEQ`.  
  
 The output value is affected by the setting of the `LC_CTYPE` category setting of the locale; see [setlocale](../vs140/setlocale--_wsetlocale.md) for more information. The versions of these functions without the `_l` suffix use the current locale for this locale-dependent behavior; the versions with the `_l` suffix are identical except that they use the locale parameter passed in instead. For more information, see [Locale](../vs140/Locale.md).  
  
## Requirements  
  
|Routine|Required header|  
|-------------|---------------------|  
|`strlen`|<string.h>|  
|`wcslen`|<string.h> or <wchar.h>|  
|`_mbslen`, `_mbslen_l`|<mbstring.h>|  
|`_mbstrlen`, `_mbstrlen_l`|<stdlib.h>|  
  
 For additional compatibility information, see [Compatibility](../vs140/Compatibility.md).  
  
## Example  
  
```  
// crt_strlen.c  
// Determine the length of a string. For the multi-byte character  
// example to work correctly, the Japanese language support for  
// non-Unicode programs must be enabled by the operating system.  
  
#include <string.h>  
#include <locale.h>  
  
int main()  
{  
   char* str1 = "Count.";  
   wchar_t* wstr1 = L"Count.";  
   char * mbstr1;  
   char * locale_string;  
  
   // strlen gives the length of single-byte character string  
   printf("Length of '%s' : %d\n", str1, strlen(str1) );  
  
   // wstrlen gives the length of a wide character string  
   wprintf(L"Length of '%s' : %d\n", wstr1, wcslen(wstr1) );  
  
   // A multibyte string: [A] [B] [C] [katakana A] [D] [\0]  
   // in Code Page 932. For this example to work correctly,  
   // the Japanese language support must be enabled by the  
   // operating system.  
   mbstr1 = "ABC" "\x83\x40" "D";  
  
   locale_string = setlocale(LC_CTYPE, "Japanese_Japan");  
  
   if (locale_string == NULL)  
   {  
      printf("Japanese locale not enabled. Exiting.\n");  
      exit(1);  
   }  
   else  
   {  
      printf("Locale set to %s\n", locale_string);  
   }  
  
   // _mbslen will recognize the Japanese multibyte character if the  
   // current locale used by the operating system is Japanese  
   printf("Length of '%s' : %d\n", mbstr1, _mbslen(mbstr1) );  
  
   // _mbstrlen will recognize the Japanese multibyte character  
   // since the CRT locale is set to Japanese even if the OS locale  
   // isnot.   
   printf("Length of '%s' : %d\n", mbstr1, _mbstrlen(mbstr1) );  
   printf("Bytes in '%s' : %d\n", mbstr1, strlen(mbstr1) );     
  
}  
```  
  
 **Length of 'Count.' : 6**  
**Length of 'Count.' : 6**  
**Length of 'ABCァD' : 5**  
**Length of 'ABCァD' : 5**  
**Bytes in 'ABCァD' : 6**   
## .NET Framework Equivalent  
 [System::String::Length](https://msdn.microsoft.com/en-us/library/system.string.length.aspx)  
  
## See Also  
 [String Manipulation](../vs140/String-Manipulation--CRT-.md)   
 [Interpretation of Multibyte-Character Sequences](../vs140/Interpretation-of-Multibyte-Character-Sequences.md)   
 [Locale](../vs140/Locale.md)   
 [setlocale, _wsetlocale](../vs140/setlocale--_wsetlocale.md)   
 [strcat, wcscat, _mbscat](../vs140/strcat--wcscat--_mbscat.md)   
 [strcmp, wcscmp, _mbscmp](../vs140/strcmp--wcscmp--_mbscmp.md)   
 [strcoll Functions](../vs140/strcoll-Functions.md)   
 [strcpy, wcscpy, _mbscpy](../vs140/strcpy--wcscpy--_mbscpy.md)   
 [strrchr, wcsrchr, _mbsrchr, _mbsrchr_l](../vs140/strrchr--wcsrchr--_mbsrchr--_mbsrchr_l.md)   
 [_strset, _wcsset, _mbsset, _mbsset_l](../vs140/_strset--_strset_l--_wcsset--_wcsset_l--_mbsset--_mbsset_l.md)   
 [strspn, wcsspn, _mbsspn, _mbsspn_l](../vs140/strspn--wcsspn--_mbsspn--_mbsspn_l.md)