---
title: "strncpy_s, _strncpy_s_l, wcsncpy_s, _wcsncpy_s_l, _mbsncpy_s, _mbsncpy_s_l"
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
  - _mbsncpy_s_l
  - wcsncpy_s
  - _strncpy_s_l
  - strncpy_s
  - _mbsncpy_s
  - _wcsncpy_s_l
apilocation: 
  - msvcr110.dll
  - msvcr90.dll
  - msvcrt.dll
  - msvcr100.dll
  - msvcr110_clr0400.dll
  - msvcr80.dll
  - msvcr120.dll
  - msvcr120_clr0400.dll
apitype: DLLExport
ms.assetid: a971c800-94d1-4d88-92f3-a2fe236a4546
caps.latest.revision: 47
translation.priority.ht: 
  - de-de
  - ja-jp
---
# strncpy_s, _strncpy_s_l, wcsncpy_s, _wcsncpy_s_l, _mbsncpy_s, _mbsncpy_s_l
Copies characters of one string to another.  These versions of [strncpy, _strncpy_l, wcsncpy, _wcsncpy_l, _mbsncpy, _mbsncpy_l](../vs140/strncpy--_strncpy_l--wcsncpy--_wcsncpy_l--_mbsncpy--_mbsncpy_l.md) have security enhancements, as described in [Security Enhancements in the CRT](../vs140/Security-Features-in-the-CRT.md).  
  
> [!IMPORTANT]
>  `_mbsncpy_s` and `_mbsncpy_s_l` cannot be used in applications that execute in the Windows Runtime. For more information, see [CRT functions not supported with /ZW](http://msdn.microsoft.com/library/windows/apps/jj606124.aspx).  
  
## Syntax  
  
```  
errno_t strncpy_s(  
   char *strDest,  
   size_t numberOfElements,  
   const char *strSource,  
   size_t count  
);  
errno_t _strncpy_s_l(  
   char *strDest,  
   size_t numberOfElements,  
   const char *strSource,  
   size_t count,  
   _locale_t locale  
);  
errno_t wcsncpy_s(  
   wchar_t *strDest,  
   size_t numberOfElements,  
   const wchar_t *strSource,  
   size_t count   
);  
errno_t _wcsncpy_s_l(  
   wchar_t *strDest,  
   size_t numberOfElements,  
   const wchar_t *strSource,  
   size_t count,  
   _locale_t locale  
);  
errno_t _mbsncpy_s(  
   unsigned char *strDest,  
   size_t numberOfElements,  
   const unsigned char *strSource,  
   size_t count   
);  
errno_t _mbsncpy_s_l(  
   unsigned char *strDest,  
   size_t numberOfElements,  
   const unsigned char *strSource,  
   size_t count,  
   locale_t locale  
);  
template <size_t size>  
errno_t strncpy_s(  
   char (&strDest)[size],  
   const char *strSource,  
   size_t count  
); // C++ only  
template <size_t size>  
errno_t _strncpy_s_l(  
   char (&strDest)[size],  
   const char *strSource,  
   size_t count,  
   _locale_t locale  
); // C++ only  
template <size_t size>  
errno_t wcsncpy_s(  
   wchar_t (&strDest)[size],  
   const wchar_t *strSource,  
   size_t count   
); // C++ only  
template <size_t size>  
errno_t _wcsncpy_s_l(  
   wchar_t (&strDest)[size],  
   const wchar_t *strSource,  
   size_t count,  
   _locale_t locale  
); // C++ only  
template <size_t size>  
errno_t _mbsncpy_s(  
   unsigned char (&strDest)[size],  
   const unsigned char *strSource,  
   size_t count   
); // C++ only  
template <size_t size>  
errno_t _mbsncpy_s_l(  
   unsigned char (&strDest)[size],  
   const unsigned char *strSource,  
   size_t count,  
   locale_t locale  
); // C++ only  
```  
  
#### Parameters  
 `strDest`  
 Destination string.  
  
 `numberOfElements`  
 The size of the destination string, in characters.  
  
 `strSource`  
 Source string.  
  
 `count`  
 Number of characters to be copied, or [_TRUNCATE](../vs140/_TRUNCATE.md).  
  
 `locale`  
 The locale to use.  
  
## Return Value  
 Zero if successful, `STRUNCATE` if truncation occurred, otherwise an error code.  
  
### Error Conditions  
  
|`strDest`|`numberOfElements`|`strSource`|Return value|Contents of `strDest`|  
|---------------|------------------------|-----------------|------------------|---------------------------|  
|`NULL`|any|any|`EINVAL`|not modified|  
|any|any|`NULL`|`EINVAL`|`strDest`[0] set to 0|  
|any|0|any|`EINVAL`|not modified|  
|not `NULL`|too small|any|`ERANGE`|`strDest`[0] set to 0|  
  
## Remarks  
 These functions try to copy the first `D` characters of `strSource` to `strDest`, where `D` is the lesser of `count` and the length of `strSource`. If those `D` characters will fit within `strDest` (whose size is given as `numberOfElements`) and still leave room for a null terminator, then those characters are copied and a terminating null is appended; otherwise, `strDest`[0] is set to the null character and the invalid parameter handler is invoked, as described in [Parameter Validation](../vs140/Parameter-Validation.md).  
  
 There is an exception to the above paragraph. If `count` is `_TRUNCATE`, then as much of `strSource` as will fit into `strDest` is copied while still leaving room for the terminating null which is always appended.  
  
 For example,  
  
 `char dst[5];`  
  
 `strncpy_s(dst, 5, "a long string", 5);`  
  
 means that we are asking `strncpy_s` to copy five characters into a buffer five bytes long; this would leave no space for the null terminator, hence `strncpy_s` zeroes out the string and calls the invalid parameter handler.  
  
 If truncation behavior is needed, use `_TRUNCATE` or (`size` – 1):  
  
 `strncpy_s(dst, 5, "a long string", _TRUNCATE);`  
  
 `strncpy_s(dst, 5, "a long string", 4);`  
  
 Note that unlike `strncpy`, if `count` is greater than the length of `strSource`, the destination string is NOT padded with null characters up to length `count`.  
  
 The behavior of `strncpy_s` is undefined if the source and destination strings overlap.  
  
 If `strDest` or `strSource` is `NULL`, or `numberOfElements` is 0, the invalid parameter handler is invoked. If execution is allowed to continue, the function returns `EINVAL` and sets `errno` to `EINVAL`.  
  
 `wcsncpy_s` and `_mbsncpy_s` are wide-character and multibyte-character versions of `strncpy_s`. The arguments and return value of `wcsncpy_s` and `mbsncpy_s`do vary accordingly. These six functions behave identically otherwise.  
  
 The output value is affected by the setting of the `LC_CTYPE` category setting of the locale; see [setlocale](../vs140/setlocale--_wsetlocale.md) for more information. The versions of these functions without the `_l` suffix use the current locale for this locale-dependent behavior; the versions with the `_l` suffix are identical except that they use the locale parameter passed in instead. For more information, see [Locale](../vs140/Locale.md).  
  
 In C++, using these functions is simplified by template overloads; the overloads can infer buffer length automatically (eliminating the need to specify a size argument) and they can automatically replace older, non-secure functions with their newer, secure counterparts. For more information, see [Secure Template Overloads](../vs140/Secure-Template-Overloads.md).  
  
 The debug versions of these functions first fill the buffer with 0xFD. To disable this behavior, use [_CrtSetDebugFillThreshold](../vs140/_CrtSetDebugFillThreshold.md).  
  
### Generic-Text Routine Mappings  
  
|TCHAR.H routine|_UNICODE & _MBCS not defined|_MBCS defined|_UNICODE defined|  
|---------------------|------------------------------------|--------------------|-----------------------|  
|`_tcsncpy_s`|`strncpy_s`|`_mbsnbcpy_s`|`wcsncpy_s`|  
|`_tcsncpy_s_l`|`_strncpy_s_l`|`_mbsnbcpy_s_l`|`_wcsncpy_s_l`|  
  
> [!NOTE]
>  _strncpy_s_l, `_wcsncpy_s_l` and `_mbsncpy_s_l` have no locale dependence and are provided just for `_tcsncpy_s_l` and are not intended to be called directly.  
  
## Requirements  
  
|Routine|Required header|  
|-------------|---------------------|  
|`strncpy_s`, `_strncpy_s_l`|<string.h>|  
|`wcsncpy_s`, `_wcsncpy_s_l`|<string.h> or <wchar.h>|  
|`_mbsncpy_s`, `_mbsncpy_s_l`|<mbstring.h>|  
  
 For additional compatibility information, see [Compatibility](../vs140/Compatibility.md).  
  
## Example  
  
```  
// crt_strncpy_s_1.cpp  
// compile with: /MTd  
  
// these #defines enable secure template overloads  
// (see last part of Examples() below)  
#define _CRT_SECURE_CPP_OVERLOAD_STANDARD_NAMES 1   
#define _CRT_SECURE_CPP_OVERLOAD_STANDARD_NAMES_COUNT 1  
  
#include <stdio.h>  
#include <stdlib.h>  
#include <string.h>  
#include <crtdbg.h>  // For _CrtSetReportMode  
#include <errno.h>  
  
// This example uses a 10-byte destination buffer.  
  
errno_t strncpy_s_tester( const char * src,  
                          int count )  
{  
   char dest[10];  
  
   printf( "\n" );  
  
   if ( count == _TRUNCATE )  
      printf( "Copying '%s' to %d-byte buffer dest with truncation semantics\n",  
               src, _countof(dest) );  
   else  
      printf( "Copying %d chars of '%s' to %d-byte buffer dest\n",  
              count, src, _countof(dest) );  
  
   errno_t err = strncpy_s( dest, _countof(dest), src, count );  
  
   printf( "    new contents of dest: '%s'\n", dest );  
  
   return err;  
}  
  
void Examples()  
{  
   strncpy_s_tester( "howdy", 4 );  
   strncpy_s_tester( "howdy", 5 );  
   strncpy_s_tester( "howdy", 6 );  
  
   printf( "\nDestination buffer too small:\n" );  
   strncpy_s_tester( "Hi there!!", 10 );  
  
   printf( "\nTruncation examples:\n" );  
  
   errno_t err = strncpy_s_tester( "How do you do?", _TRUNCATE );  
   printf( "    truncation %s occur\n", err == STRUNCATE ? "did"  
                                                       : "did not" );  
  
   err = strncpy_s_tester( "Howdy.", _TRUNCATE );  
   printf( "    truncation %s occur\n", err == STRUNCATE ? "did"  
                                                       : "did not" );  
  
   printf( "\nSecure template overload example:\n" );  
  
   char dest[10];  
   strncpy( dest, "very very very long", 15 );  
   // With secure template overloads enabled (see #defines at  
   // top of file), the preceding line is replaced by  
   //    strncpy_s( dest, _countof(dest), "very very very long", 15 );  
   // Instead of causing a buffer overrun, strncpy_s invokes  
   // the invalid parameter handler.  
   // If secure template overloads were disabled, strncpy would  
   // copy 15 characters and overrun the dest buffer.  
   printf( "    new contents of dest: '%s'\n", dest );  
}  
  
void myInvalidParameterHandler(  
   const wchar_t* expression,  
   const wchar_t* function,   
   const wchar_t* file,   
   unsigned int line,   
   uintptr_t pReserved)  
{  
   wprintf(L"Invalid parameter handler invoked: %s\n", expression);  
}  
  
int main( void )  
{  
   _invalid_parameter_handler oldHandler, newHandler;  
  
   newHandler = myInvalidParameterHandler;  
   oldHandler = _set_invalid_parameter_handler(newHandler);  
   // Disable the message box for assertions.  
   _CrtSetReportMode(_CRT_ASSERT, 0);  
  
   Examples();  
}  
```  
  
 **Copying 4 chars of 'howdy' to 10-byte buffer dest**  
 **new contents of dest: 'howd'**  
**Copying 5 chars of 'howdy' to 10-byte buffer dest**  
 **new contents of dest: 'howdy'**  
**Copying 6 chars of 'howdy' to 10-byte buffer dest**  
 **new contents of dest: 'howdy'**  
**Destination buffer too small:**  
**Copying 10 chars of 'Hi there!!' to 10-byte buffer dest**  
**Invalid parameter handler invoked: (L"Buffer is too small" && 0)**  
 **new contents of dest: ''**  
**Truncation examples:**  
**Copying 'How do you do?' to 10-byte buffer dest with truncation semantics**  
 **new contents of dest: 'How do yo'**  
 **truncation did occur**  
**Copying 'Howdy.' to 10-byte buffer dest with truncation semantics**  
 **new contents of dest: 'Howdy.'**  
 **truncation did not occur**  
**Secure template overload example:**  
**Invalid parameter handler invoked: (L"Buffer is too small" && 0)**  
 **new contents of dest: ''**   
## Example  
  
```  
// crt_strncpy_s_2.c  
// contrasts strncpy and strncpy_s  
  
#include <stdio.h>  
#include <stdlib.h>  
  
int main( void )  
{  
   char a[20] = "test";  
   char s[20];  
  
   // simple strncpy usage:  
  
   strcpy_s( s, 20, "dogs like cats" );  
   printf( "Original string:\n   '%s'\n", s );  
  
   // Here we can't use strncpy_s since we don't   
   // want null termination  
   strncpy( s, "mice", 4 );  
   printf( "After strncpy (no null-termination):\n   '%s'\n", s );  
   strncpy( s+5, "love", 4 );  
   printf( "After strncpy into middle of string:\n   '%s'\n", s );  
  
   // If we use strncpy_s, the string is terminated   
   strncpy_s( s, _countof(s), "mice", 4 );  
   printf( "After strncpy_s (with null-termination):\n   '%s'\n", s );  
  
}  
```  
  
 **Original string:**  
 **'dogs like cats'**  
**After strncpy (no null-termination):**  
 **'mice like cats'**  
**After strncpy into middle of string:**  
 **'mice love cats'**  
**After strncpy_s (with null-termination):**  
 **'mice'**   
## .NET Framework Equivalent  
 [System::String::Copy](https://msdn.microsoft.com/en-us/library/system.string.copy.aspx)  
  
## See Also  
 [String Manipulation](../vs140/String-Manipulation--CRT-.md)   
 [Locale](../vs140/Locale.md)   
 [Interpretation of Multibyte-Character Sequences](../vs140/Interpretation-of-Multibyte-Character-Sequences.md)   
 [_mbsnbcpy, _mbsnbcpy_l](../vs140/_mbsnbcpy--_mbsnbcpy_l.md)   
 [strcat_s, wcscat_s, _mbscat_s](../vs140/strcat_s--wcscat_s--_mbscat_s.md)   
 [strcmp, wcscmp, _mbscmp](../vs140/strcmp--wcscmp--_mbscmp.md)   
 [strcpy_s, wcscpy_s, _mbscpy_s](../vs140/strcpy_s--wcscpy_s--_mbscpy_s.md)   
 [strncat_s, _strncat_s_l, wcsncat_s, _wcsncat_s_l, _mbsncat_s, _mbsncat_s_l](../vs140/strncat_s--_strncat_s_l--wcsncat_s--_wcsncat_s_l--_mbsncat_s--_mbsncat_s_l.md)   
 [strncmp, wcsncmp, _mbsncmp, _mbsncmp_l](../vs140/strncmp--wcsncmp--_mbsncmp--_mbsncmp_l.md)   
 [_strnicmp, _wcsnicmp, _mbsnicmp, _strnicmp_l, _wcsnicmp_l, _mbsnicmp_l](../vs140/_strnicmp--_wcsnicmp--_mbsnicmp--_strnicmp_l--_wcsnicmp_l--_mbsnicmp_l.md)   
 [strrchr, wcsrchr, _mbsrchr, _mbsrchr_l](../vs140/strrchr--wcsrchr--_mbsrchr--_mbsrchr_l.md)   
 [_strset, _wcsset, _mbsset, _mbsset_l](../vs140/_strset--_strset_l--_wcsset--_wcsset_l--_mbsset--_mbsset_l.md)   
 [strspn, wcsspn, _mbsspn, _mbsspn_l](../vs140/strspn--wcsspn--_mbsspn--_mbsspn_l.md)