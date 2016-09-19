---
title: "_vsprintf_p, _vsprintf_p_l, _vswprintf_p, _vswprintf_p_l"
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
  - _vsprintf_p
  - _vswprintf_p
  - _vsprintf_p_l
  - _vswprintf_p_l
apilocation: 
  - msvcr90.dll
  - msvcr110_clr0400.dll
  - msvcr120.dll
  - msvcr110.dll
  - msvcr100.dll
  - msvcrt.dll
  - msvcr80.dll
apitype: DLLExport
ms.assetid: 00821c0d-9fee-4d8a-836c-0669cfb11317
caps.latest.revision: 20
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _vsprintf_p, _vsprintf_p_l, _vswprintf_p, _vswprintf_p_l
Write formatted output using a pointer to a list of arguments, with the ability to specify the order in which the arguments are used.  
  
## Syntax  
  
```  
int _vsprintf_p(  
   char *buffer,  
   size_t sizeInBytes,  
   const char *format,  
   va_list argptr   
);   
int _vsprintf_p_l(  
   char *buffer,  
   size_t sizeInBytes,  
   const char *format,  
   locale_t locale,  
   va_list argptr   
);   
int _vswprintf_p(  
   wchar_t *buffer,  
   size_t count,  
   const wchar_t *format,  
   va_list argptr   
);  
int _vswprintf_p_l(  
   wchar_t *buffer,  
   size_t count,  
   const wchar_t *format,  
   locale_t locale,  
   va_list argptr   
);  
```  
  
#### Parameters  
 `buffer`  
 Storage location for output.  
  
 `sizeInBytes`  
 Size of `buffer` in characters.  
  
 `count`  
 Maximum number of characters to store, in the UNICODE version of this function.  
  
 `format`  
 Format specification.  
  
 `argptr`  
 Pointer to list of arguments.  
  
 `locale`  
 The locale to use.  
  
## Return Value  
 `_vsprintf_p` and `_vswprintf_p` return the number of characters written, not including the terminating null character, or a negative value if an output error occurs.  
  
## Remarks  
 Each of these functions takes a pointer to an argument list, and then formats and writes the given data to the memory pointed to by `buffer`.  
  
 These functions differ from the `vsprintf_s` and `vswprintf_s` only in that they support positional parameters. For more information, see [printf Positional Parameters](../vs140/printf_p-Positional-Parameters.md).  
  
 The versions of these functions with the `_l` suffix are identical except that they use the locale parameter passed in instead of the current thread locale.  
  
 If the `buffer` or `format` parameters are NULL pointers, if count is zero, or if the format string contains invalid formatting characters, the invalid parameter handler is invoked, as described in [Parameter Validation](../vs140/Parameter-Validation.md). If execution is allowed to continue, the functions return -1 and set `errno` to `EINVAL`.  
  
### Generic-Text Routine Mappings  
  
|TCHAR.H routine|_UNICODE & _MBCS not defined|_MBCS defined|_UNICODE defined|  
|---------------------|------------------------------------|--------------------|-----------------------|  
|`_vstprintf_p`|`_vsprintf_p`|`_vsprintf_p`|`_vswprintf_p`|  
|`_vstprintf_p_l`|`_vsprintf_p_l`|`_vsprintf_p_l`|`_vswprintf_p_l`|  
  
## Requirements  
  
|Routine|Required header|Optional headers|  
|-------------|---------------------|----------------------|  
|`_vsprintf_p`, `_vsprintf_p_l`|<stdio.h> and <stdarg.h>|<varargs.h>*|  
|`_vswprintf_p`, `_vswprintf_p_l`|<stdio.h> or <wchar.h>, and <stdarg.h>|<varargs.h>*|  
  
 \* Required for UNIX V compatibility.  
  
 For additional compatibility information, see [Compatibility](../vs140/Compatibility.md) in the Introduction.  
  
## Example  
  
```  
// crt__vsprintf_p.c  
// This program uses vsprintf_p to write to a buffer.  
// The size of the buffer is determined by _vscprintf_p.  
  
#include <stdlib.h>  
#include <stdio.h>  
#include <stdarg.h>  
  
void example( char * format, ... )  
{  
    va_list  args;  
    int      len;  
    char     *buffer = NULL;  
  
    va_start( args, format );  
  
    // _vscprintf doesn't count the   
    // null terminating string so we add 1.  
    len = _vscprintf_p( format, args ) + 1;  
  
    // Allocate memory for our buffer  
    buffer = (char*)malloc( len * sizeof(char) );  
    if (buffer)  
    {  
        _vsprintf_p( buffer, len, format, args );  
        puts( buffer );  
        free( buffer );  
    }  
}  
  
int main( void )  
{  
    // First example  
    example( "%2$d %1$c %3$d", '<', 123, 456 );  
  
    // Second example  
    example( "%s", "This is a string" );  
}  
```  
  
 **123 < 456**  
**This is a string**   
## .NET Framework Equivalent  
 [System::String::Format](https://msdn.microsoft.com/en-us/library/system.string.format.aspx)  
  
## See Also  
 [Stream I/O](../vs140/Stream-I-O.md)   
 [vprintf Functions](../vs140/vprintf-Functions.md)   
 [Format Specification Syntax: printf and wprintf Functions](../vs140/Format-Specification-Syntax--printf-and-wprintf-Functions.md)   
 [fprintf, fwprintf](../vs140/fprintf--_fprintf_l--fwprintf--_fwprintf_l.md)   
 [printf, wprintf](../vs140/printf--_printf_l--wprintf--_wprintf_l.md)   
 [sprintf, swprintf](../vs140/sprintf--_sprintf_l--swprintf--_swprintf_l--__swprintf_l.md)   
 [va_arg, va_end, va_start](../vs140/va_arg--va_copy--va_end--va_start.md)