---
title: "wcrtomb_s"
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
  - wcrtomb_s
apilocation: 
  - msvcr120.dll
  - msvcr100.dll
  - msvcr110_clr0400.dll
  - msvcr80.dll
  - msvcr90.dll
  - msvcrt.dll
  - msvcr110.dll
apitype: DLLExport
ms.assetid: 9a8a1bd0-1d60-463d-a3a2-d83525eaf656
caps.latest.revision: 22
translation.priority.mt: 
  - de-de
  - ja-jp
---
# wcrtomb_s
Convert a wide character into its multibyte character representation. A version of [wcrtomb](../vs140/wcrtomb.md) with security enhancements as described in [Security Enhancements in the CRT](../vs140/Security-Features-in-the-CRT.md).  
  
## Syntax  
  
```  
errno_t wcrtomb_s(  
   size_t *pReturnValue,  
   char *mbchar,  
   size_t sizeOfmbchar,  
   wchar_t *wchar,  
   mbstate_t *mbstate  
);  
template <size_t size>  
errno_t wcrtomb_s(  
   size_t *pReturnValue,  
   char (&mbchar)[size],  
   wchar_t *wchar,  
   mbstate_t *mbstate  
); // C++ only  
```  
  
#### Parameters  
 [out] `pReturnValue`  
 Returns the number of bytes written or -1 if an error occurred.  
  
 [out] `mbchar`  
 The resulting multibyte converted character.  
  
 [in] `sizeOfmbchar`  
 The size of the `mbchar` variable in bytes.  
  
 [in] `wchar`  
 A wide character to convert.  
  
 [in] `mbstate`  
 A pointer to an `mbstate_t` object.  
  
## Return Value  
 Returns zero or an `errno` value if an error occurs.  
  
## Remarks  
 The `wcrtomb_s` function converts a wide character, beginning in the specified conversion state contained in `mbstate`, from the value contained in `wchar`, into the address represented by `mbchar`. The `pReturnValue` value will be the number of bytes converted, but no more than `MB_CUR_MAX` bytes, or an -1 if an error occurred.  
  
 If `mbstate` is null, the internal `mbstate_t` conversion state is used. If the character contained in `wchar` does not have a corresponding multibyte character, the value of `pReturnValue` will be -1 and the function will return the `errno` value of `EILSEQ`.  
  
 The `wcrtomb_s` function differs from [wctomb_s](../vs140/wctomb_s--_wctomb_s_l.md) by its restartability. The conversion state is stored in `mbstate` for subsequent calls to the same or other restartable functions. Results are undefined when mixing the use of restartable and nonrestartable functions. For example, an application would use `wcsrlen` rather than `wcslen`, if a subsequent call to `wcsrtombs_s` were used instead of `wcstombs_s.`  
  
 In C++, using this function is simplified by template overloads; the overloads can infer buffer length automatically (eliminating the need to specify a size argument) and they can automatically replace older, non-secure functions with their newer, secure counterparts. For more information, see [Secure Template Overloads](../vs140/Secure-Template-Overloads.md).  
  
## Exceptions  
 The `wcrtomb_s` function is multithread safe as long as no function in the current thread calls `setlocale` while this function is executing and the `mbstate` is null.  
  
## Example  
  
```  
// crt_wcrtomb_s.c  
// This program converts a wide character  
// to its corresponding multibyte character.  
//  
  
#include <string.h>  
#include <stdio.h>  
#include <wchar.h>  
  
int main( void )  
{  
    errno_t     returnValue;  
    size_t      pReturnValue;  
    mbstate_t   mbstate;  
    size_t      sizeOfmbStr = 1;  
    char        mbchar = 0;  
    wchar_t*    wchar = L"Q\0";  
  
    // Reset to initial conversion state  
    memset(&mbstate, 0, sizeof(mbstate));  
  
    returnValue = wcrtomb_s(&pReturnValue, &mbchar, sizeof(char),  
                            *wchar, &mbstate);  
    if (returnValue == 0) {  
        printf("The corresponding wide character \"");  
        wprintf(L"%s\"", wchar);  
        printf(" was converted to a the \"%c\" ", mbchar);  
        printf("multibyte character.\n");  
    }  
    else  
    {  
        printf("No corresponding multibyte character "  
               "was found.\n");  
    }  
}  
```  
  
 **The corresponding wide character "Q" was converted to a the "Q" multibyte character.**   
## .NET Framework Equivalent  
 Not applicable. To call the standard C function, use `PInvoke`. For more information, see [Platform Invoke Examples](assetId:///15926806-f0b7-487e-93a6-4e9367ec689f).  
  
## Requirements  
  
|Routine|Required header|  
|-------------|---------------------|  
|`wcrtomb_s`|<wchar.h>|  
  
## See Also  
 [Data Conversion](../vs140/Data-Conversion.md)   
 [Locale](../vs140/Locale.md)   
 [Interpretation of Multibyte-Character Sequences](../vs140/Interpretation-of-Multibyte-Character-Sequences.md)   
 [mbsinit](../vs140/mbsinit.md)