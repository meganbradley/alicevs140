---
title: "_mbclen, mblen, _mblen_l"
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
  - _mbclen
  - mblen
  - _mblen_l
apilocation: 
  - msvcr120.dll
  - msvcr110.dll
  - msvcr80.dll
  - msvcr100.dll
  - msvcrt.dll
  - msvcr90.dll
  - msvcr110_clr0400.dll
apitype: DLLExport
ms.assetid: d5eb92a0-b7a3-464a-aaf7-9890a8e3ed70
caps.latest.revision: 26
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _mbclen, mblen, _mblen_l
Gets the length and determines the validity of a multibyte character.  
  
> [!IMPORTANT]
>  This API cannot be used in applications that execute in the Windows Runtime. For more information, see [CRT functions not supported with /ZW](http://msdn.microsoft.com/library/windows/apps/jj606124.aspx).  
  
## Syntax  
  
```  
size_t _mbclen(  
   const unsigned char *c   
);  
int mblen(  
   const char *mbstr,  
   size_t count   
);  
int _mblen_l(  
   const char *mbstr,  
   size_t count,  
   _locale_t locale  
);  
```  
  
#### Parameters  
 `c`  
 Multibyte character.  
  
 `mbstr`  
 Address of a multibyte-character byte sequence.  
  
 `count`  
 Number of bytes to check.  
  
 `locale`  
 Locale to use.  
  
## Return Value  
 `_mbclen` returns 1 or 2, according to whether the multibyte character `c` is 1 or 2 bytes long. There is no error return for `_mbclen`. If `mbstr` is not `NULL`, `mblen` returns the length, in bytes, of the multibyte character. If `mbstr` is `NULL` or it points to the wide-character null character, `mblen` returns 0. If the object that `mbstr` points to does not form a valid multibyte character within the first `count` characters, `mblen` returns –1.  
  
## Remarks  
 The `_mbclen` function returns the length, in bytes, of the multibyte character `c`. If `c` does not point to the lead byte of a multibyte character as determined by an implicit call to `_ismbblead`, the result of `_mbclen` is unpredictable.  
  
 `mblen` returns the length in bytes of `mbstr` if it is a valid multibyte character and determines multibyte-character validity associated with the code page. `mblen` examines `count` or fewer bytes contained in `mbstr`, but not more than `MB_CUR_MAX` bytes.  
  
 The output value is affected by the setting of the `LC_CTYPE` category setting of the locale; see [setlocale](../vs140/setlocale--_wsetlocale.md) for more information. The versions of these functions without the `_l` suffix use the current locale for this locale-dependent behavior; the versions with the `_l` suffix are identical except that they use the locale parameter passed in instead. For more information, see [Locale](../vs140/Locale.md).  
  
### Generic-Text Routine Mappings  
  
|Tchar.h routine|_UNICODE and _MBCS not defined|_MBCS defined|_UNICODE defined|  
|---------------------|--------------------------------------|--------------------|-----------------------|  
|`_tclen`|Maps to macro or inline function|`_mbclen`|Maps to macro or inline function|  
  
## Requirements  
  
|Routine|Required header|  
|-------------|---------------------|  
|`_mbclen`|<mbstring.h>|  
|`mblen`|<stdlib.h>|  
|`_mblen_l`|<stdlib.h>|  
  
 For more compatibility information, see [Compatibility](../vs140/Compatibility.md).  
  
## Example  
  
```  
// crt_mblen.c  
/* illustrates the behavior of the mblen function  
 */  
  
#include <stdlib.h>  
#include <stdio.h>  
  
int main( void )  
{  
    int      i;  
    char    *pmbc = (char *)malloc( sizeof( char ) );  
    wchar_t  wc   = L'a';  
  
    printf( "Convert wide character to multibyte character:\n" );  
    wctomb_s( &i, pmbc, sizeof(char), wc );  
    printf( "  Characters converted: %u\n", i );  
    printf( "  Multibyte character: %x\n\n", *pmbc );  
  
    i = mblen( pmbc, MB_CUR_MAX );  
    printf( "Length in bytes of multibyte character %x: %u\n", *pmbc, i );  
  
    pmbc = NULL;  
    i = mblen( pmbc, MB_CUR_MAX );  
    printf( "Length in bytes of NULL multibyte character %x: %u\n", pmbc, i );  
}  
```  
  
## Output  
  
```  
Convert wide character to multibyte character:  
  Characters converted: 1  
  Multibyte character: 61  
  
Length in bytes of multibyte character 61: 1  
Length in bytes of NULL multibyte character 0: 0  
```  
  
## .NET Framework Equivalent  
 Not applicable. To call the standard C function, use `PInvoke`. For more information, see [Platform Invoke Examples](assetId:///15926806-f0b7-487e-93a6-4e9367ec689f).  
  
## See Also  
 [Character Classification](../vs140/Character-Classification.md)   
 [Locale](../vs140/Locale.md)   
 [Interpretation of Multibyte-Character Sequences](../vs140/Interpretation-of-Multibyte-Character-Sequences.md)   
 [_mbccpy, _mbccpy_l](../vs140/_mbccpy--_mbccpy_l.md)   
 [strlen, strlen_l, wcslen, wcslen_l, _mbslen, _mbslen_l, _mbstrlen, _mbstrlen_l](../vs140/strlen--wcslen--_mbslen--_mbslen_l--_mbstrlen--_mbstrlen_l.md)