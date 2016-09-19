---
title: "sprintf, _sprintf_l, swprintf, _swprintf_l, __swprintf_l"
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
  - __swprintf_l
  - sprintf
  - _sprintf_l
  - _swprintf_l
  - swprintf
apilocation: 
  - msvcrt.dll
  - msvcr80.dll
  - msvcr120.dll
  - msvcr110.dll
  - msvcr110_clr0400.dll
  - msvcr100.dll
  - msvcr90.dll
apitype: DLLExport
ms.assetid: f6efe66f-3563-4c74-9455-5411ed939b81
caps.latest.revision: 36
translation.priority.ht: 
  - de-de
  - ja-jp
---
# sprintf, _sprintf_l, swprintf, _swprintf_l, __swprintf_l
Write formatted data to a string. More secure versions of some of these functions are available; see [sprintf_s, _sprintf_s_l, swprintf_s, _swprintf_s_l](../vs140/sprintf_s--_sprintf_s_l--swprintf_s--_swprintf_s_l.md). The secure versions of `swprintf` and `_swprintf_l` do not take a `count` parameter.  
  
## Syntax  
  
```  
int sprintf(  
   char *buffer,  
   const char *format [,  
   argument] ...   
);  
int _sprintf_l(  
   char *buffer,  
   const char *format,  
   locale_t locale [,  
   argument] ...   
);  
int swprintf(  
   wchar_t *buffer,  
   size_t count,  
   const wchar_t *format [,  
   argument]...  
);  
int _swprintf_l(  
   wchar_t *buffer,  
   size_t count,  
   const wchar_t *format,  
   locale_t locale [,  
   argument] ...   
);  
int __swprintf_l(  
   wchar_t *buffer,  
   const wchar_t *format,  
   locale_t locale [,  
   argument] ...   
);  
template <size_t size>  
int sprintf(  
   char (&buffer)[size],  
   const char *format [,  
   argument] ...   
); // C++ only  
template <size_t size>  
int _sprintf_l(  
   char (&buffer)[size],  
   const char *format,  
   locale_t locale [,  
   argument] ...   
); // C++ only  
  
```  
  
#### Parameters  
 `buffer`  
 Storage location for output  
  
 `count`  
 Maximum number of characters to store in the Unicode version of this function.  
  
 `format`  
 Format-control string  
  
 `argument`  
 Optional arguments  
  
 `locale`  
 The locale to use.  
  
 For more information, see [Format Specifications](../vs140/Format-Specification-Syntax--printf-and-wprintf-Functions.md).  
  
## Return Value  
 The number of characters written, or –1 if an error occurred. If `buffer` or `format` is a null pointer, the invalid parameter handler is invoked, as described in [Parameter Validation](../vs140/Parameter-Validation.md). If execution is allowed to continue, these functions return -1 and set `errno` to `EINVAL`.  
  
 `sprintf` returns the number of bytes stored in `buffer`, not counting the terminating null character. `swprintf`returns the number of wide characters stored in `buffer`, not counting the terminating null wide character.  
  
## Remarks  
 The `sprintf` function formats and stores a series of characters and values in `buffer`. Each `argument` (if any) is converted and output according to the corresponding format specification in `format`. The format consists of ordinary characters and has the same form and function as the `format` argument for [printf](../vs140/printf--_printf_l--wprintf--_wprintf_l.md). A null character is appended after the last character written. If copying occurs between strings that overlap, the behavior is undefined.  
  
> [!IMPORTANT]
>  Using `sprintf`, there is no way to limit the number of characters written, which means that code using `sprintf` is susceptible to buffer overruns. Consider using the related function [_snprintf](../vs140/snprintf--_snprintf--_snprintf_l--_snwprintf--_snwprintf_l.md), which specifies a maximum number of characters to be written to `buffer`, or use [_scprintf](../vs140/_scprintf--_scprintf_l--_scwprintf--_scwprintf_l.md) to determine how large a buffer is required. Also, ensure that `format` is not a user-defined string.  
  
 `swprintf` is a wide-character version of `sprintf`; the pointer arguments to `swprintf` are wide-character strings. Detection of encoding errors in `swprintf` may differ from that in `sprintf`. `swprintf` and `fwprintf` behave identically except that `swprintf` writes output to a string rather than to a destination of type `FILE`, and `swprintf` requires the `count` parameter to specify the maximum number of characters to be written. The versions of these functions with the `_l` suffix are identical except that they use the locale parameter passed in instead of the current thread locale.  
  
 `swprintf` conforms to the ISO C Standard, which requires the second parameter, `count`, of type `size_t`. To force the old nonstandard behavior, define `_CRT_NON_CONFORMING_SWPRINTFS`. In a future version, the old behavior may be removed, so code should be changed to use the new conformant behavior.  
  
 In C++, these functions have template overloads that invoke the newer, secure counterparts of these functions. For more information, see [Secure Template Overloads](../vs140/Secure-Template-Overloads.md).  
  
### Generic-Text Routine Mappings  
  
|TCHAR.H routine|_UNICODE & _MBCS not defined|_MBCS defined|_UNICODE defined|  
|---------------------|------------------------------------|--------------------|-----------------------|  
|`_stprintf`|`sprintf`|`sprintf`|`_swprintf`|  
|`_stprintf_l`|`_sprintf_l`|`_sprintf_l`|`__swprintf_l`|  
  
## Requirements  
  
|Routine|Required header|  
|-------------|---------------------|  
|`sprintf`, `_sprintf_l`|<stdio.h>|  
|`swprintf`, `_swprintf_l`|<stdio.h> or <wchar.h>|  
  
 For additional compatibility information, see [Compatibility](../vs140/Compatibility.md) in the Introduction.  
  
## Example  
  
```  
// crt_sprintf.c  
// compile with: /W3  
// This program uses sprintf to format various  
// data and place them in the string named buffer.  
  
#include <stdio.h>  
  
int main( void )  
{  
   char  buffer[200], s[] = "computer", c = 'l';  
   int   i = 35, j;  
   float fp = 1.7320534f;  
  
   // Format and print various data:   
   j  = sprintf( buffer,     "   String:    %s\n", s ); // C4996  
   j += sprintf( buffer + j, "   Character: %c\n", c ); // C4996  
   j += sprintf( buffer + j, "   Integer:   %d\n", i ); // C4996  
   j += sprintf( buffer + j, "   Real:      %f\n", fp );// C4996  
   // Note: sprintf is deprecated; consider using sprintf_s instead  
  
   printf( "Output:\n%s\ncharacter count = %d\n", buffer, j );  
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
// crt_swprintf.c  
// wide character example  
// also demonstrates swprintf returning error code  
#include <stdio.h>  
  
int main( void )  
{  
   wchar_t buf[100];  
   int len = swprintf( buf, 100, L"%s", L"Hello world" );  
   printf( "wrote %d characters\n", len );  
   len = swprintf( buf, 100, L"%s", L"Hello\xffff world" );  
   // swprintf fails because string contains WEOF (\xffff)  
   printf( "wrote %d characters\n", len );  
}  
```  
  
 **wrote 11 characters**  
**wrote -1 characters**   
## .NET Framework Equivalent  
 [System::String::Format](https://msdn.microsoft.com/en-us/library/system.string.format.aspx)  
  
## See Also  
 [Stream I/O](../vs140/Stream-I-O.md)   
 [fprintf, fwprintf](../vs140/fprintf--_fprintf_l--fwprintf--_fwprintf_l.md)   
 [printf, wprintf](../vs140/printf--_printf_l--wprintf--_wprintf_l.md)   
 [scanf, wscanf](../vs140/scanf--_scanf_l--wscanf--_wscanf_l.md)   
 [sscanf, swscanf](../vs140/sscanf--_sscanf_l--swscanf--_swscanf_l.md)   
 [vprintf Functions](../vs140/vprintf-Functions.md)