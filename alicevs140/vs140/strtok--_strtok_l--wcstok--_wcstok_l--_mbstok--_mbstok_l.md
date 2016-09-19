---
title: "strtok, _strtok_l, wcstok, _wcstok_l, _mbstok, _mbstok_l"
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
  - _mbstok_l
  - _mbstok
  - wcstok
  - _mbstok
  - strtok
  - _wcstok_l
apilocation: 
  - msvcr80.dll
  - msvcrt.dll
  - msvcr120.dll
  - msvcr100.dll
  - msvcr110_clr0400.dll
  - msvcr110.dll
  - msvcr90.dll
apitype: DLLExport
ms.assetid: 904cb734-f0d7-4d77-ba81-4791ddf461ae
caps.latest.revision: 34
translation.priority.ht: 
  - de-de
  - ja-jp
---
# strtok, _strtok_l, wcstok, _wcstok_l, _mbstok, _mbstok_l
Finds the next token in a string, by using the current locale or a specified locale that's passed in. More secure versions of these functions are available; see [strtok_s, _strtok_s_l, wcstok_s, _wcstok_s_l, _mbstok_s, _mbstok_s_l](../vs140/strtok_s--_strtok_s_l--wcstok_s--_wcstok_s_l--_mbstok_s--_mbstok_s_l.md).  
  
> [!IMPORTANT]
>  `_mbstok` and `_mbstok_l` cannot be used in applications that execute in the Windows Runtime. For more information, see [CRT functions not supported with /ZW](http://msdn.microsoft.com/library/windows/apps/jj606124.aspx).  
  
## Syntax  
  
```  
char *strtok(  
   char *strToken,  
   const char *strDelimit   
);  
wchar_t *wcstok(  
   wchar_t *strToken,  
   const wchar_t *strDelimit   
);  
unsigned char *_mbstok(  
   unsigned char*strToken,  
   const unsigned char *strDelimit   
);  
unsigned char *_mbstok(  
   unsigned char*strToken,  
   const unsigned char *strDelimit,  
   _locale_t locale  
);  
```  
  
#### Parameters  
 `strToken`  
 String containing token or tokens.  
  
 `strDelimit`  
 Set of delimiter characters.  
  
 `locale`  
 Locale to use.  
  
## Return Value  
 Returns a pointer to the next token found in `strToken`. They return `NULL` when no more tokens are found. Each call modifies `strToken` by substituting a `NULL` character for the first delimiter that occurs after the returned token.  
  
## Remarks  
 The `strtok` function finds the next token in `strToken`. The set of characters in `strDelimit` specifies possible delimiters of the token to be found in `strToken` on the current call. `wcstok` and `_mbstok` are wide-character and multibyte-character versions of `strtok`. The arguments and return value of `wcstok` are wide-character strings; those of `_mbstok` are multibyte-character strings. These three functions behave identically otherwise.  
  
> [!IMPORTANT]
>  These functions incur a potential threat brought about by a buffer overrun problem. Buffer overrun problems are a frequent method of system attack, resulting in an unwarranted elevation of privilege. For more information, see [Avoiding Buffer Overruns](http://msdn.microsoft.com/library/windows/desktop/ms717795).  
  
 On the first call to `strtok`, the function skips leading delimiters and returns a pointer to the first token in `strToken`, terminating the token with a null character. More tokens can be broken out of the remainder of `strToken` by a series of calls to `strtok`. Each call to `strtok`modifies `strToken` by inserting a null character after the `token` returned by that call. To read the next token from `strToken`, call `strtok` with a `NULL` value for the `strToken` argument. The `NULL` `strToken` argument causes `strtok` to search for the next token in the modified `strToken`. The `strDelimit` argument can take any value from one call to the next so that the set of delimiters may vary.  
  
 The output value is affected by the setting of the `LC_CTYPE` category setting of the locale; see [setlocale](../vs140/setlocale--_wsetlocale.md) for more information. The versions of these functions without the `_l` suffix use the current locale for this locale-dependent behavior; the versions with the `_l` suffix are identical except that they use the locale parameter passed in instead. For more information, see [Locale](../vs140/Locale.md).  
  
> [!NOTE]
>  Each function uses a thread-local static variable for parsing the string into tokens. Therefore, multiple threads can simultaneously call these functions without undesirable effects. However, within a single thread, interleaving calls to one of these functions is highly likely to produce data corruption and inaccurate results. When parsing different strings, finish parsing one string before starting to parse the next. Also, be aware of the potential for danger when calling one of these functions from within a loop where another function is called. If the other function ends up using one of these functions, an interleaved sequence of calls will result, triggering data corruption.  
  
### Generic-Text Routine Mappings  
  
|TCHAR.H routine|_UNICODE & _MBCS not defined|_MBCS defined|_UNICODE defined|  
|---------------------|------------------------------------|--------------------|-----------------------|  
|`_tcstok`|`strtok`|`_mbstok`|`wcstok`|  
|`_tcstok`|`_strtok_l`|`_mbstok_l`|`_wcstok_l`|  
  
## Requirements  
  
|Routine|Required header|  
|-------------|---------------------|  
|`strtok`|<string.h>|  
|`wcstok`|<string.h> or <wchar.h>|  
|`_mbstok`, `_mbstok_l`|<mbstring.h>|  
  
 For additional compatibility information, see [Compatibility](../vs140/Compatibility.md).  
  
## Example  
  
```  
// crt_strtok.c  
// compile with: /W3  
// In this program, a loop uses strtok  
// to print all the tokens (separated by commas  
// or blanks) in the string named "string".  
//  
#include <string.h>  
#include <stdio.h>  
  
char string[] = "A string\tof ,,tokens\nand some  more tokens";  
char seps[]   = " ,\t\n";  
char *token;  
  
int main( void )  
{  
   printf( "Tokens:\n" );  
  
   // Establish string and get the first token:  
   token = strtok( string, seps ); // C4996  
   // Note: strtok is deprecated; consider using strtok_s instead  
   while( token != NULL )  
   {  
      // While there are tokens in "string"  
      printf( " %s\n", token );  
  
      // Get next token:   
      token = strtok( NULL, seps ); // C4996  
   }  
}  
```  
  
 **Tokens:**  
 **A**  
 **string**  
 **of**  
 **tokens**  
 **and**  
 **some**  
 **more**  
 **tokens**   
## .NET Framework Equivalent  
 Not applicable. To call the standard C function, use `PInvoke`. For more information, see [Platform Invoke Examples](assetId:///15926806-f0b7-487e-93a6-4e9367ec689f).  
  
## See Also  
 [String Manipulation](../vs140/String-Manipulation--CRT-.md)   
 [Locale](../vs140/Locale.md)   
 [Interpretation of Multibyte-Character Sequences](../vs140/Interpretation-of-Multibyte-Character-Sequences.md)   
 [strcspn, wcscspn, _mbscspn, _mbscspn_l](../vs140/strcspn--wcscspn--_mbscspn--_mbscspn_l.md)   
 [strspn, wcsspn, _mbsspn, _mbsspn_l](../vs140/strspn--wcsspn--_mbsspn--_mbsspn_l.md)