---
title: "strnlen, strnlen_s, wcsnlen, wcsnlen_s, _mbsnlen, _mbsnlen_l, _mbstrnlen, _mbstrnlen_l"
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
  - wcsnlen
  - strnlen_s
  - _mbstrnlen
  - _mbsnlen_l
  - _mbstrnlen_l
  - strnlen
  - wcsnlen_s
  - _mbsnlen
apilocation: 
  - msvcr120.dll
  - msvcr110_clr0400.dll
  - msvcr90.dll
  - msvcr100.dll
  - msvcr110.dll
  - msvcr80.dll
  - msvcrt.dll
  - api-ms-win-crt-string-l1-1-0.dll
apitype: DLLExport
ms.assetid: cc05ce1c-72ea-4ae4-a7e7-4464e56e5f80
caps.latest.revision: 35
translation.priority.ht: 
  - de-de
  - ja-jp
---
# strnlen, strnlen_s, wcsnlen, wcsnlen_s, _mbsnlen, _mbsnlen_l, _mbstrnlen, _mbstrnlen_l
Gets the length of a string by using the current locale or one that has been passed in. These are more secure versions of [strlen, wcslen, _mbslen, _mbstrlen](../vs140/strlen--wcslen--_mbslen--_mbslen_l--_mbstrlen--_mbstrlen_l.md).  
  
> [!IMPORTANT]
>  `_mbsnlen`, `_mbsnlen_l`, `_mbstrnlen`, and `_mbstrnlen_l` cannot be used in applications that execute in the [!INCLUDE[wrt](../vs140/includes/wrt_md.md)]. For more information, see [CRT functions not supported with /ZW](http://msdn.microsoft.com/library/windows/apps/jj606124.aspx).  
  
## Syntax  
  
```  
size_t strnlen(  
   const char *str,  
   size_t numberOfElements   
);  
size_t strnlen_s(  
   const char *str,  
   size_t numberOfElements   
);  
size_t wcsnlen(  
   const wchar_t *str,  
   size_t numberOfElements  
);  
size_t wcsnlen_s(  
   const wchar_t *str,  
   size_t numberOfElements  
);  
size_t _mbsnlen(  
   const unsigned char *str,  
   size_t numberOfElements  
);  
size_t _mbsnlen_l(  
   const unsigned char *str,  
   size_t numberOfElements,  
   _locale_t locale  
);  
size_t _mbstrnlen(  
   const char *str,  
   size_t numberOfElements  
);  
size_t _mbstrnlen_l(  
   const char *str,  
   size_t numberOfElements,  
   _locale_t locale  
);  
```  
  
#### Parameters  
 `str`  
 Null-terminated string.  
  
 `numberOfElements`  
 The size of the string buffer.  
  
 `locale`  
 Locale to use.  
  
## Return Value  
 These functions return the number of characters in the string, not including the terminating null character. If there is no null terminator within the first `numberOfElements` bytes of the string (or wide characters for `wcsnlen`), then `numberOfElements` is returned to indicate the error condition; null-terminated strings have lengths that are strictly less than `numberOfElements`.  
  
 `_mbstrnlen` and `_mbstrnlen_l` return -1 if the string contains an invalid multibyte character.  
  
## Remarks  
  
> [!NOTE]
>  `strnlen` is not a replacement for `strlen`; `strnlen` is intended to be used only to calculate the size of incoming untrusted data in a buffer of known size—for example, a network packet. `strnlen` calculates the length but doesn't walk past the end of the buffer if the string is unterminated. For other situations, use `strlen`. (The same applies to `wcsnlen`, `_mbsnlen`, and `_mbstrnlen`.)  
  
 Each of these functions returns the number of characters in `str`, not including the terminating null character. However, `strnlen` and `strnlen_s` interpret the string as a single-byte character string and therefore, the return value is always equal to the number of bytes, even if the string contains multibyte characters. `wcsnlen` and `wcsnlen_s` are wide-character versions of `strnlen` and `strnlen_s` respectively; the arguments for `wcsnlen` and `wcsnlen_s` are wide-character strings and the count of characters are in wide-character units. Otherwise, `wcsnlen` and `strnlen` behave identically, as do `strnlen_s` and `wcsnlen_s`.  
  
 `strnlen`, `wcsnlen,` and `_mbsnlen` do not validate their parameters. If `str` is `NULL`, an access violation occurs.  
  
 `strnlen_s` and `wcsnlen_s` validate their parameters. If `str` is `NULL`, the functions return 0.  
  
 `_mbstrnlen` also validates its parameters. If `str` is `NULL`, or if `numberOfElements` is greater than `INT_MAX`, `_mbstrnlen` generates an invalid parameter exception, as described in [Parameter Validation](../vs140/Parameter-Validation.md). If execution is allowed to continue, `_mbstrnlen` sets `errno` to `EINVAL` and returns -1.  
  
### Generic-Text Routine Mappings  
  
|TCHAR.H routine|_UNICODE & _MBCS not defined|_MBCS defined|_UNICODE defined|  
|---------------------|------------------------------------|--------------------|-----------------------|  
|`_tcsnlen`|`strnlen`|`strnlen`|`wcsnlen`|  
|`_tcscnlen`|`strnlen`|`_mbsnlen`|`wcsnlen`|  
|`_tcscnlen_l`|`strnlen`|`_mbsnlen_l`|`wcsnlen`|  
  
 `_mbsnlen` and `_mbstrnlen` return the number of multibyte characters in a multibyte-character string. `_mbsnlen` recognizes multibyte-character sequences according to the multibyte code page that's currently in use or according to the locale that's passed in; it does not test for multibyte-character validity. `_mbstrnlen` tests for multibyte-character validity and recognizes multibyte-character sequences. If the string that's passed to `_mbstrnlen` contains an invalid multibyte character, `errno` is set to `EILSEQ`.  
  
 The output value is affected by the setting of the `LC_CTYPE` category setting of the locale; see [setlocale, _wsetlocale](../vs140/setlocale--_wsetlocale.md) for more information. The versions of these functions are identical, except that the ones that don't have the `_l` suffix use the current locale for this locale-dependent behavior and the versions that have the `_l` suffix instead use the locale parameter that's passed in. For more information, see [Locale](../vs140/Locale.md).  
  
## Requirements  
  
|Routine|Required header|  
|-------------|---------------------|  
|`strnlen`, `strnlen_s`|<string.h>|  
|`wcsnlen`, `wcsnlen_s`|<string.h> or <wchar.h>|  
|`_mbsnlen`, `_mbsnlen_l`|<mbstring.h>|  
|`_mbstrnlen`, `_mbstrnlen_l`|<stdlib.h>|  
  
 For additional compatibility information, see [Compatibility](../vs140/Compatibility.md).  
  
## Example  
  
```  
  
      // crt_strnlen.c  
  
#include <string.h>  
  
int main()  
{  
   // str1 is 82 characters long. str2 is 159 characters long   
  
   char* str1 = "The length of a string is the number of characters\n"  
               "excluding the terminating null.";  
   char* str2 = "strnlen takes a maximum size. If the string is longer\n"  
                "than the maximum size specified, the maximum size is\n"  
                "returned rather than the actual size of the string.";  
   size_t len;  
   size_t maxsize = 100;  
  
   len = strnlen(str1, maxsize);  
   printf("%s\n Length: %d \n\n", str1, len);  
  
   len = strnlen(str2, maxsize);  
   printf("%s\n Length: %d \n", str2, len);  
}  
```  
  
 **The length of a string is the number of characters**  
**excluding the terminating null.**  
 **Length: 82**   
**strnlen takes a maximum size. If the string is longer**  
**than the maximum size specified, the maximum size is**  
**returned rather than the actual size of the string.**  
 **Length: 100**    
## .NET Framework Equivalent  
 [System::String::Length](https://msdn.microsoft.com/en-us/library/system.string.length.aspx)  
  
## See Also  
 [String Manipulation](../vs140/String-Manipulation--CRT-.md)   
 [Locale](../vs140/Locale.md)   
 [Interpretation of Multibyte-Character Sequences](../vs140/Interpretation-of-Multibyte-Character-Sequences.md)   
 [setlocale, _wsetlocale](../vs140/setlocale--_wsetlocale.md)   
 [strncat, _strncat_l, wcsncat, _wcsncat_l, _mbsncat _mbsncat_l](../vs140/strncat--_strncat_l--wcsncat--_wcsncat_l--_mbsncat--_mbsncat_l.md)   
 [strncmp, wcsncmp, _mbsncmp, _mbsncmp_l](../vs140/strncmp--wcsncmp--_mbsncmp--_mbsncmp_l.md)   
 [strcoll Functions](../vs140/strcoll-Functions.md)   
 [strncpy_s, _strncpy_s_l, wcsncpy_s, _wcsncpy_s_l, _mbsncpy_s, \__mbsncpy_s_l](../vs140/strncpy_s--_strncpy_s_l--wcsncpy_s--_wcsncpy_s_l--_mbsncpy_s--_mbsncpy_s_l.md)   
 [strrchr, wcsrchr, _mbsrchr, _mbsrchr_l](../vs140/strrchr--wcsrchr--_mbsrchr--_mbsrchr_l.md)   
 [_strset, _strset_l, _wcsset, _wcsset_l, _mbsset, _mbsset_l](../vs140/_strset--_strset_l--_wcsset--_wcsset_l--_mbsset--_mbsset_l.md)   
 [strspn, wcsspn, _mbsspn, _mbsspn_l](../vs140/strspn--wcsspn--_mbsspn--_mbsspn_l.md)