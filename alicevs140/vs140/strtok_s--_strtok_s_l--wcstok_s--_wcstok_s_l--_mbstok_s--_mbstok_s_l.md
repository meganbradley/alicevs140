---
title: "strtok_s, _strtok_s_l, wcstok_s, _wcstok_s_l, _mbstok_s, _mbstok_s_l"
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
  - _wcstok_s_l
  - _mbstok_s_l
  - _mbstok_s
  - strtok_s
  - wcstok_s
  - _strtok_s_l
apilocation: 
  - msvcr120.dll
  - msvcr110.dll
  - msvcr110_clr0400.dll
  - msvcr100.dll
  - msvcr80.dll
  - msvcrt.dll
  - msvcr90.dll
apitype: DLLExport
ms.assetid: 7696c972-f83b-4617-8c82-95973e9fdb46
caps.latest.revision: 28
translation.priority.ht: 
  - de-de
  - ja-jp
---
# strtok_s, _strtok_s_l, wcstok_s, _wcstok_s_l, _mbstok_s, _mbstok_s_l
Finds the next token in a string, by using the current locale or a locale that's passed in. These versions of [strtok, _strtok_l, wcstok, _wcstok_l, _mbstok, _mbstok_l](../vs140/strtok--_strtok_l--wcstok--_wcstok_l--_mbstok--_mbstok_l.md) have security enhancements, as described in [Security Enhancements in the CRT](../vs140/Security-Features-in-the-CRT.md).  
  
> [!IMPORTANT]
>  `_mbstok_s` and `_mbstok_s_l` cannot be used in applications that execute in the Windows Runtime. For more information, see [CRT functions not supported with /ZW](http://msdn.microsoft.com/library/windows/apps/jj606124.aspx).  
  
## Syntax  
  
```  
  
      char *strtok_s(  
char *strToken,  
const char *strDelimit,  
   char **context  
);  
char *_strtok_s_l(  
char *strToken,  
const char *strDelimit,  
   char **context,  
_locale_tlocale  
);  
wchar_t *wcstok_s(  
wchar_t *strToken,  
const wchar_t *strDelimit,   
   wchar_t**context  
);  
wchar_t *_wcstok_s_l(  
wchar_t *strToken,  
const wchar_t *strDelimit,   
   wchar_t**context,  
_locale_tlocale  
);  
unsigned char *_mbstok_s(  
unsigned char*strToken,  
const unsigned char *strDelimit,   
   char **context  
);  
unsigned char *_mbstok_s(  
unsigned char*strToken,  
const unsigned char *strDelimit,   
   char **context,  
_locale_tlocale  
);  
```  
  
#### Parameters  
 `strToken`  
 String containing token or tokens.  
  
 `strDelimit`  
 Set of delimiter characters.  
  
 `context`  
 Used to store position information between calls to `strtok_s`  
  
 `locale`  
 Locale to use.  
  
## Return Value  
 Returns a pointer to the next token found in `strToken`. They return `NULL` when no more tokens are found. Each call modifies `strToken` by substituting a `NULL` character for the first delimiter that occurs after the returned token.  
  
### Error Conditions  
  
|`strToken`|`strDelimit`|`context`|Return value|`errno`|  
|----------------|------------------|---------------|------------------|-------------|  
|`NULL`|any|pointer to a null pointer|`NULL`|`EINVAL`|  
|any|`NULL`|any|`NULL`|`EINVAL`|  
|any|any|`NULL`|`NULL`|`EINVAL`|  
  
 If `strToken` is `NULL` but context is a pointer to a valid context pointer, there is no error.  
  
## Remarks  
 The `strtok_s` function finds the next token in `strToken`. The set of characters in `strDelimit` specifies possible delimiters of the token to be found in `strToken` on the current call. `wcstok_s` and `_mbstok_s`are wide-character and multibyte-character versions of `strtok_s`. The arguments and return values of `wcstok_s` and `_wcstok_s_l` are wide-character strings; those of `_mbstok_s` and `_mbstok_s_l` are multibyte-character strings. These three functions behave identically otherwise.  
  
 This function validates its parameters. If an error condition occurs, as in the Error Conditions table, the invalid parameter handler is invoked, as described in [Parameter Validation](../vs140/Parameter-Validation.md). If execution is allowed to continue, these functions set `errno` to `EINVAL` and return `NULL`.  
  
### Generic-Text Routine Mappings  
  
|TCHAR.H routine|_UNICODE & _MBCS not defined|_MBCS defined|_UNICODE defined|  
|---------------------|------------------------------------|--------------------|-----------------------|  
|`_tcstok_s`|`strtok_s`|`_mbstok_s`|`wcstok_s`|  
|`_tcstok_s_l`|`_strtok_s_l`|`_mbstok_s_l`|`_wcstok_s_l`|  
  
 On the first call to `strtok_s` the function skips leading delimiters and returns a pointer to the first token in `strToken`, terminating the token with a null character. More tokens can be broken out of the remainder of `strToken` by a series of calls to `strtok_s`. Each call to `strtok_s` modifies `strToken` by inserting a null character after the token returned by that call. The `context` pointer keeps track of which string is being read and where in the string the next token is to be read. To read the next token from `strToken`, call `strtok_s` with a `NULL` value for the `strToken` argument, and pass the same `context` parameter. The `NULL` `strToken` argument causes `strtok_s` to search for the next token in the modified `strToken`. The `strDelimit` argument can take any value from one call to the next so that the set of delimiters may vary.  
  
 Since the `context` parameter supersedes the static buffers used in `strtok` and `_strtok_l`, it is possible to parse two strings simultaneously in the same thread.  
  
 The output value is affected by the setting of the `LC_CTYPE` category setting of the locale; see [setlocale](../vs140/setlocale--_wsetlocale.md) for more information. The versions of these functions without the `_l` suffix use the current locale for this locale-dependent behavior; the versions with the `_l` suffix are identical except that they use the locale parameter passed in instead. For more information, see [Locale](../vs140/Locale.md).  
  
## Requirements  
  
|Routine|Required header|  
|-------------|---------------------|  
|`strtok_s`|<string.h>|  
|`_strtok_s_l`|<string.h>|  
|`wcstok_s,`<br /><br /> `_wcstok_s_l`|<string.h> or <wchar.h>|  
|`_mbstok_s,`<br /><br /> `_mbstok_s_l`|<mbstring.h>|  
  
 For additional compatibility information, see [Compatibility](../vs140/Compatibility.md).  
  
## Example  
  
```  
// crt_strtok_s.c  
// In this program, a loop uses strtok_s  
// to print all the tokens (separated by commas  
// or blanks) in two strings at the same time.  
//  
  
#include <string.h>  
#include <stdio.h>  
  
char string1[] =  
    "A string\tof ,,tokens\nand some  more tokens";  
char string2[] =  
    "Another string\n\tparsed at the same time.";  
char seps[]   = " ,\t\n";  
char *token1 = NULL;  
char *token2 = NULL;  
char *next_token1 = NULL;  
char *next_token2 = NULL;  
  
int main( void )  
{  
    printf( "Tokens:\n" );  
  
    // Establish string and get the first token:  
    token1 = strtok_s( string1, seps, &next_token1);  
    token2 = strtok_s ( string2, seps, &next_token2);  
  
    // While there are tokens in "string1" or "string2"  
    while ((token1 != NULL) || (token2 != NULL))  
    {  
        // Get next token:  
        if (token1 != NULL)  
        {  
            printf( " %s\n", token1 );  
            token1 = strtok_s( NULL, seps, &next_token1);  
        }  
        if (token2 != NULL)  
        {  
            printf("        %s\n", token2 );  
            token2 = strtok_s (NULL, seps, &next_token2);  
        }  
    }  
}  
```  
  
 **Tokens:**  
 **A**  
 **Another**  
 **string**  
 **string**  
 **of**  
 **parsed**  
 **tokens**  
 **at**  
 **and**  
 **the**  
 **some**  
 **same**  
 **more**  
 **time.**  
 **tokens**   
## .NET Framework Equivalent  
 Not applicable. To call the standard C function, use `PInvoke`. For more information, see [Platform Invoke Examples](assetId:///15926806-f0b7-487e-93a6-4e9367ec689f).  
  
## See Also  
 [String Manipulation](../vs140/String-Manipulation--CRT-.md)   
 [Locale](../vs140/Locale.md)   
 [Interpretation of Multibyte-Character Sequences](../vs140/Interpretation-of-Multibyte-Character-Sequences.md)   
 [strcspn, wcscspn, _mbscspn, _mbscspn_l](../vs140/strcspn--wcscspn--_mbscspn--_mbscspn_l.md)   
 [strspn, wcsspn, _mbsspn, _mbsspn_l](../vs140/strspn--wcsspn--_mbsspn--_mbsspn_l.md)