---
title: "_sprintf_p, _sprintf_p_l, _swprintf_p, _swprintf_p_l"
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
  - _sprintf_p
  - _swprintf_p_l
  - _swprintf_p
  - _sprintf_p_l
apilocation: 
  - msvcrt.dll
  - msvcr110_clr0400.dll
  - msvcr120.dll
  - msvcr80.dll
  - msvcr90.dll
  - msvcr110.dll
  - msvcr100.dll
apitype: DLLExport
ms.assetid: a2ae78e8-6b0c-48d5-87a9-ea2365b0693d
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _sprintf_p, _sprintf_p_l, _swprintf_p, _swprintf_p_l
Write formatted data to a string with the ability to specify the order that the parameters are used in the format string.  
  
## Syntax  
  
```  
int _sprintf_p(  
   char *buffer,  
   size_t sizeOfBuffer,  
   const char *format [,  
   argument] ...   
);  
int _sprintf_p_l(  
   char *buffer,  
   size_t sizeOfBuffer,  
   const char *format,  
   locale_t locale [,  
   argument] ...   
);  
int _swprintf_p(  
   wchar_t *buffer,  
   size_t sizeOfBuffer,  
   const wchar_t *format [,  
   argument]...  
);  
int _swprintf_p_l(  
   wchar_t *buffer,  
   size_t sizeOfBuffer,  
   const wchar_t *format,  
   locale_t locale [,  
   argument] …   
);  
```  
  
#### Parameters  
 `buffer`  
 Storage location for output  
  
 `sizeOfBuffer`  
 Maximum number of characters to store.  
  
 `format`  
 Format-control string  
  
 `argument`  
 Optional arguments  
  
 `locale`  
 The locale to use.  
  
 For more information, see [Format Specifications](../vs140/Format-Specification-Syntax--printf-and-wprintf-Functions.md).  
  
## Return Value  
 The number of characters written, or –1 if an error occurred.  
  
## Remarks  
 The `_sprintf_p` function formats and stores a series of characters and values in `buffer`. Each `argument` (if any) is converted and output according to the corresponding format specification in `format`. The format consists of ordinary characters and has the same form and function as the `format` argument for `printf_p`. A `NULL` character is appended after the last character written. If copying occurs between strings that overlap, the behavior is undefined. The difference between `_sprintf_p` and `sprintf_s` is that `_sprintf_p` supports positional parameters, which allows specifying the order in which the arguments are used in the format string. For more information, see [printf Positional Parameters](../vs140/printf_p-Positional-Parameters.md).  
  
 `_swprintf_p` is a wide-character version of `_sprintf_p`; the pointer arguments to `_swprintf_p` are wide-character strings. Detection of encoding errors in `_swprintf_p` may differ from that in `_sprintf_p`. `_swprintf_p` and `fwprintf_p` behave identically except that `_swprintf_p` writes output to a string rather than to a destination of type `FILE`, and `_swprintf_p` requires the `count`parameter to specify the maximum number of characters to be written. The versions of these functions with the `_l` suffix are identical except that they use the locale parameter passed in instead of the current thread locale.  
  
 `_sprintf_p` returns the number of bytes stored in `buffer`, not counting the terminating `NULL` character. `_swprintf_p`returns the number of wide characters stored in `buffer`, not counting the terminating `NULL` wide character. If `buffer` or `format` is a null pointer, or if the format string contains invalid formatting characters, the invalid parameter handler is invoked, as described in [Parameter Validation](../vs140/Parameter-Validation.md). If execution is allowed to continue, these functions return -1 and set `errno` to `EINVAL`.  
  
### Generic-Text Routine Mappings  
  
|TCHAR.H routine|_UNICODE & _MBCS not defined|_MBCS defined|_UNICODE defined|  
|---------------------|------------------------------------|--------------------|-----------------------|  
|`_stprintf_p`|`_sprintf_p`|`_sprintf_p`|`_swprintf_p`|  
|`_stprintf_p_l`|`_sprintf_p_l`|`_sprintf_p_l`|`_swprintf_p_l`|  
  
## Requirements  
  
|Routine|Required header|  
|-------------|---------------------|  
|`_sprintf_p`, `_sprintf_p_l`|<stdio.h>|  
|`_swprintf_p`, `_swprintf_p_l`|<stdio.h> or <wchar.h>|  
  
 For additional compatibility information, see [Compatibility](../vs140/Compatibility.md) in the Introduction.  
  
## Example  
  
```  
// crt_sprintf_p.c  
// This program uses _sprintf_p to format various  
// data and place them in the string named buffer.  
//  
  
#include <stdio.h>  
  
int main( void )  
{  
    char     buffer[200],  
            s[] = "computer", c = 'l';  
    int      i = 35,  
            j;  
    float    fp = 1.7320534f;  
  
    // Format and print various data:   
    j  = _sprintf_p( buffer, 200,  
                     "   String:    %s\n", s );  
    j += _sprintf_p( buffer + j, 200 - j,   
                     "   Character: %c\n", c );  
    j += _sprintf_p( buffer + j, 200 - j,   
                     "   Integer:   %d\n", i );  
    j += _sprintf_p( buffer + j, 200 - j,   
                     "   Real:      %f\n", fp );  
  
    printf( "Output:\n%s\ncharacter count = %d\n",   
            buffer, j );  
}  
```  
  
 **Output:**  
 **String:    computer**  
 **Character: l**  
 **Integer:   35**  
 **Real:      1.732053**  
**character count = 79**   
## Example  
  
```  
// crt_swprintf_p.c  
// This is the wide character example which  
// also demonstrates _swprintf_p returning  
// error code.  
#include <stdio.h>  
  
#define BUFFER_SIZE 100  
  
int main( void )  
{  
    wchar_t buffer[BUFFER_SIZE];  
    int     len;  
  
    len = _swprintf_p(buffer, BUFFER_SIZE, L"%2$s %1$d",  
                      0, L" marbles in your head.");  
    _printf_p( "Wrote %d characters\n", len );  
  
    // _swprintf_p fails because string contains WEOF (\xffff)  
    len = _swprintf_p(buffer, BUFFER_SIZE, L"%s",   
                      L"Hello\xffff world" );  
    _printf_p( "Wrote %d characters\n", len );  
}  
```  
  
 **Wrote 24 characters**  
**Wrote -1 characters**   
## .NET Framework Equivalent  
 [System::String::Format](https://msdn.microsoft.com/en-us/library/system.string.format.aspx)  
  
## See Also  
 [Stream I/O](../vs140/Stream-I-O.md)   
 [_fprintf_p, _fwprintf_p](../vs140/_fprintf_p--_fprintf_p_l--_fwprintf_p--_fwprintf_p_l.md)   
 [fprintf, fwprintf](../vs140/fprintf--_fprintf_l--fwprintf--_fwprintf_l.md)   
 [_printf_p, _wprintf_p](../vs140/_printf_p--_printf_p_l--_wprintf_p--_wprintf_p_l.md)   
 [printf, wprintf](../vs140/printf--_printf_l--wprintf--_wprintf_l.md)   
 [scanf, wscanf](../vs140/scanf--_scanf_l--wscanf--_wscanf_l.md)   
 [sscanf, swscanf](../vs140/sscanf--_sscanf_l--swscanf--_swscanf_l.md)   
 [sscanf_s, swscanf_s](../vs140/sscanf_s--_sscanf_s_l--swscanf_s--_swscanf_s_l.md)   
 [vprintf Functions](../vs140/vprintf-Functions.md)   
 [printf Positional Parameters](../vs140/printf_p-Positional-Parameters.md)