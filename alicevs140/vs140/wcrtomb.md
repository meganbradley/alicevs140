---
title: "wcrtomb"
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
  - wcrtomb
apilocation: 
  - msvcr80.dll
  - msvcr110.dll
  - msvcr90.dll
  - msvcr100.dll
  - msvcr120.dll
  - msvcr110_clr0400.dll
  - msvcrt.dll
apitype: DLLExport
ms.assetid: 717f1b21-2705-4b7f-b6d0-82adc5224340
caps.latest.revision: 26
translation.priority.ht: 
  - de-de
  - ja-jp
---
# wcrtomb
Convert a wide character into its multibyte character representation. A more secure version of this function is available; see [wcrtomb_s](../vs140/wcrtomb_s.md).  
  
## Syntax  
  
```  
size_t wcrtomb(  
   char *mbchar,  
   wchar_t wchar,  
   mbstate_t *mbstate  
);  
template <size_t size>  
size_t wcrtomb(  
   char (&mbchar)[size],  
   wchar_t wchar,  
   mbstate_t *mbstate  
); // C++ only  
```  
  
#### Parameters  
 [out] `mbchar`  
 The resulting multibyte converted character.  
  
 [in] `wchar`  
 A wide character to convert.  
  
 [in] `mbstate`  
 A pointer to an `mbstate_t` object.  
  
## Return Value  
 Returns the number of bytes required to represent the converted multibyte character, otherwise a -1 if an error occurs.  
  
## Remarks  
 The `wcrtomb` function converts a wide character, beginning in the specified conversion state contained in `mbstate`, from the value contained in `wchar`, into the address represented by `mbchar`. The return value is the number of bytes required to represent the corresponding multibyte character, but it will not return more than `MB_CUR_MAX` bytes.  
  
 If `mbstate` is null, the internal `mbstate_t` object containing the conversion state of `mbchar` is used. If the character sequence `wchar` does not have a corresponding multibyte character representation, a -1 is returned and the `errno` is set to `EILSEQ`.  
  
 The `wcrtomb` function differs from [wctomb](../vs140/wctomb--_wctomb_l.md) by its restartability. The conversion state is stored in `mbstate` for subsequent calls to the same or other restartable functions. Results are undefined when mixing the use of restartable and nonrestartable functions. For example, an application would use `wcsrlen` rather than `wcsnlen`, if a subsequent call to `wcsrtombs` were used instead of `wcstombs`.  
  
 In C++, this function has a template overload that invokes the newer, secure counterparts of this function. For more information, see [Secure Template Overloads](../vs140/Secure-Template-Overloads.md).  
  
## Exceptions  
 The `wcrtomb` function is multithread safe as long as no function in the current thread calls `setlocale` while this function is executing and while the `mbstate` is null.  
  
## Example  
  
```  
// crt_wcrtomb.c  
// compile with: /W3  
// This program converts a wide character  
// to its corresponding multibyte character.  
  
#include <string.h>  
#include <stdio.h>  
#include <wchar.h>  
  
int main( void )  
{  
    size_t      sizeOfCovertion = 0;  
    mbstate_t   mbstate;  
    char        mbStr = 0;  
    wchar_t*    wcStr = L"Q";  
  
    // Reset to initial conversion state  
    memset(&mbstate, 0, sizeof(mbstate));  
  
    sizeOfCovertion = wcrtomb(&mbStr, *wcStr, &mbstate); // C4996  
    // Note: wcrtomb is deprecated; consider using wcrtomb_s instead  
    if (sizeOfCovertion > 0)  
    {  
        printf("The corresponding wide character \"");  
        wprintf(L"%s\"", wcStr);  
        printf(" was converted to the \"%c\" ", mbStr);  
        printf("multibyte character.\n");  
    }  
    else  
    {  
        printf("No corresponding multibyte character "  
               "was found.\n");  
    }  
}  
```  
  
 **The corresponding wide character "Q" was converted to the "Q" multibyte character.**   
## .NET Framework Equivalent  
 Not applicable. To call the standard C function, use `PInvoke`. For more information, see [Platform Invoke Examples](assetId:///15926806-f0b7-487e-93a6-4e9367ec689f).  
  
## Requirements  
  
|Routine|Required header|  
|-------------|---------------------|  
|`wcrtomb`|<wchar.h>|  
  
## See Also  
 [Data Conversion](../vs140/Data-Conversion.md)   
 [Locale](../vs140/Locale.md)   
 [Interpretation of Multibyte-Character Sequences](../vs140/Interpretation-of-Multibyte-Character-Sequences.md)   
 [mbsinit](../vs140/mbsinit.md)