---
title: "vsprintf, _vsprintf_l, vswprintf, _vswprintf_l, __vswprintf_l"
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
  - _vswprintf_l
  - _vsprintf_l
  - vsprintf
  - vswprintf
  - __vswprintf_l
apilocation: 
  - msvcr120.dll
  - msvcr90.dll
  - msvcr100.dll
  - msvcr80.dll
  - msvcr110.dll
  - msvcr110_clr0400.dll
  - msvcrt.dll
apitype: DLLExport
ms.assetid: b8ef1c0d-58f9-4a18-841a-f1a989e1c29b
caps.latest.revision: 32
translation.priority.ht: 
  - de-de
  - ja-jp
---
# vsprintf, _vsprintf_l, vswprintf, _vswprintf_l, __vswprintf_l
Write formatted output using a pointer to a list of arguments. More secure versions of these functions are available; see [vsprintf_s, _vsprintf_s_l, vswprintf_s, _vswprintf_s_l](../vs140/vsprintf_s--_vsprintf_s_l--vswprintf_s--_vswprintf_s_l.md).  
  
## Syntax  
  
```  
int vsprintf(  
   char *buffer,  
   const char *format,  
   va_list argptr   
);   
int _vsprintf_l(  
   char *buffer,  
   const char *format,  
   locale_t locale,  
   va_list argptr   
);   
int vswprintf(  
   wchar_t *buffer,  
   size_t count,  
   const wchar_t *format,  
   va_list argptr   
);  
int _vswprintf_l(  
   wchar_t *buffer,  
   size_t count,  
   const wchar_t *format,  
   locale_t locale,  
   va_list argptr   
);  
int __vswprintf_l(  
   wchar_t *buffer,  
   const wchar_t *format,  
   locale_t locale,  
   va_list argptr   
);  
template <size_t size>  
int vsprintf(  
   char (&buffer)[size],  
   const char *format,  
   va_list argptr   
); // C++ only  
template <size_t size>  
int _vsprintf_l(  
   char (&buffer)[size],  
   const char *format,  
   locale_t locale,  
   va_list argptr   
); // C++ only  
template <size_t size>  
int vswprintf(  
   wchar_t (&buffer)[size],  
   const wchar_t *format,  
   va_list argptr   
); // C++ only  
template <size_t size>  
int _vswprintf_l(  
   wchar_t (&buffer)[size],  
   const wchar_t *format,  
   locale_t locale,  
   va_list argptr   
); // C++ only  
```  
  
#### Parameters  
 `buffer`  
 Storage location for output.  
  
 `count`  
 Maximum number of characters to store, in the `UNICODE` version of this function.  
  
 `format`  
 Format specification.  
  
 `argptr`  
 Pointer to list of arguments.  
  
 `locale`  
 The locale to use.  
  
## Return Value  
 `vsprintf` and `vswprintf` return the number of characters written, not including the terminating null character, or a negative value if an output error occurs. If `buffer` or `format` is a null pointer, these functions invoke the invalid parameter handler, as described in [Parameter Validation](../vs140/Parameter-Validation.md). If execution is allowed to continue, these functions return -1 and set `errno` to `EINVAL`.  
  
 For information on these and other error codes, see [_doserrno, errno, _sys_errlist, and _sys_nerr](../vs140/errno--_doserrno--_sys_errlist--and-_sys_nerr.md).  
  
## Remarks  
 Each of these functions takes a pointer to an argument list, and then formats and writes the given data to the memory pointed to by `buffer`.  
  
 The versions of these functions with the `_l` suffix are identical except that they use the locale parameter passed in instead of the current thread locale.  
  
> [!IMPORTANT]
>  Using `vsprintf`, here is no way to limit the number of characters written, which means that code using this function is susceptible to buffer overruns. Use [_vsnprintf](../vs140/vsnprintf--_vsnprintf--_vsnprintf_l--_vsnwprintf--_vsnwprintf_l.md) instead, or call [_vscprintf](../vs140/_vscprintf--_vscprintf_l--_vscwprintf--_vscwprintf_l.md) to determine how large a buffer is needed. Also, ensure that `format` is not a user-defined string. For more information, see [Avoiding Buffer Overruns](http://msdn.microsoft.com/library/windows/desktop/ms717795).  
  
 `vswprintf` conforms to the ISO C Standard, which requires the second parameter, `count`, of type `size_t`. To force the old nonstandard behavior, define `_CRT_NON_CONFORMING_SWPRINTFS.` The old behavior may not be in a future version, so code should be changed to use the new conformant behavior.  
  
 In C++, these functions have template overloads that invoke the newer, secure counterparts of these functions. For more information, see [Secure Template Overloads](../vs140/Secure-Template-Overloads.md).  
  
### Generic-Text Routine Mappings  
  
|TCHAR.H routine|_UNICODE & _MBCS not defined|_MBCS defined|_UNICODE defined|  
|---------------------|------------------------------------|--------------------|-----------------------|  
|`_vstprintf`|`vsprintf`|`vsprintf`|`vswprintf`|  
|`_vstprintf_l`|`_vsprintf_l`|`_vsprintf_l`|`_vswprintf_l`|  
  
## Requirements  
  
|Routine|Required header|Optional headers|  
|-------------|---------------------|----------------------|  
|`vsprintf`, `_vsprintf_l`|<stdio.h> and <stdarg.h>|<varargs.h>*|  
|`vswprintf`, `_vswprintf_l`|<stdio.h> or <wchar.h>, and <stdarg.h>|<varargs.h>*|  
  
 \* Required for UNIX V compatibility.  
  
 For additional compatibility information, see [Compatibility](../vs140/Compatibility.md) in the Introduction.  
  
## Example  
  
```  
// crt_vsprintf.c  
// compile with: /W3  
// This program uses vsprintf to write to a buffer.  
// The size of the buffer is determined by _vscprintf.  
  
#include <stdlib.h>  
#include <stdio.h>  
#include <stdarg.h>  
  
void test( char * format, ... )  
{  
    va_list args;  
    int     len;  
    char    *buffer;  
  
    // retrieve the variable arguments  
    va_start( args, format );  
  
    len = _vscprintf( format, args ) // _vscprintf doesn't count  
                                + 1; // terminating '\0'  
  
    buffer = (char*)malloc( len * sizeof(char) );  
  
    vsprintf( buffer, format, args ); // C4996  
    // Note: vsprintf is deprecated; consider using vsprintf_s instead  
    puts( buffer );  
  
    free( buffer );  
}  
  
int main( void )  
{  
   test( "%d %c %d", 123, '<', 456 );  
   test( "%s", "This is a string" );  
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