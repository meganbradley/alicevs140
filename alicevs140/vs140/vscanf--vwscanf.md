---
title: "vscanf, vwscanf"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: article
apiname: 
  - vscanf
  - vwscanf
apilocation: 
  - msvcr80.dll
  - msvcrt.dll
  - msvcr110.dll
  - msvcr100.dll
  - msvcr110_clr0400.dll
  - msvcr120.dll
  - msvcr90.dll
apitype: DLLExport
ms.assetid: d1df595b-11bc-4682-9441-a92616301e3b
caps.latest.revision: 6
translation.priority.ht: 
  - de-de
  - ja-jp
---
# vscanf, vwscanf
Reads formatted data from the standard input stream. More secure versions of these function are available; see [vscanf_s, vwscanf_s](../vs140/vscanf_s--vwscanf_s.md).  
  
## Syntax  
  
```  
int vscanf(  
   const char *format,  
   va_list arglist  
);  
int vwscanf(  
   const wchar_t *format,  
   va_list arglist  
);  
  
```  
  
#### Parameters  
 `format`  
 Format control string.  
  
 `arglist`  
 Variable argument list.  
  
## Return Value  
 Returns the number of fields that are successfully converted and assigned; the return value does not include fields that were read but not assigned. A return value of 0 indicates that no fields were assigned.  
  
 If `format` is a `NULL` pointer, the invalid parameter handler is invoked, as described in [Parameter Validation](../vs140/Parameter-Validation.md). If execution is allowed to continue, these functions return `EOF` and set `errno` to `EINVAL`.  
  
 For information about these and other error codes, see [errno, _doserrno, _sys_errlist, and _sys_nerr](../vs140/errno--_doserrno--_sys_errlist--and-_sys_nerr.md).  
  
## Remarks  
 The `vscanf` function reads data from the standard input stream `stdin` and writes the data into the locations that are given by the `arglist` argument list. Each argument in the list must be a pointer to a variable of a type that corresponds to a type specifier in `format`. If copying occurs between strings that overlap, the behavior is undefined.  
  
> [!IMPORTANT]
>  When you use `vscanf` to read a string, always specify a width for the `%s` format (for example, `"%32s"` instead of `"%s"`); otherwise, incorrectly formatted input can cause a buffer overrun. As an alternative, you can use [vscanf_s, vwscanf_s](../vs140/vscanf_s--vwscanf_s.md) or [fgets](../vs140/fgets--fgetws.md).  
  
 `vwscanf` is a wide-character version of `vscanf`; the `format` argument to `vwscanf` is a wide-character string. `vwscanf` and `vscanf` behave identically if the stream is opened in ANSI mode. `vscanf` doesn't support input from a UNICODE stream.  
  
### Generic-Text Routine Mappings  
  
|TCHAR.H routine|_UNICODE & _MBCS not defined|_MBCS defined|_UNICODE defined|  
|---------------------|------------------------------------|--------------------|-----------------------|  
|`_vtscanf`|`vscanf`|`vscanf`|`vwscanf`|  
  
 For more information, see [Format Specification Fields: scanf and wscanf Functions](../vs140/Format-Specification-Fields--scanf-and-wscanf-Functions.md).  
  
## Requirements  
  
|Routine|Required header|  
|-------------|---------------------|  
|`vscanf`|<stdio.h>|  
|`vwscanf`|<stdio.h> or <wchar.h>|  
  
 The console is not supported in [!INCLUDE[win8_appname_long](../vs140/includes/win8_appname_long_md.md)] apps. The standard stream handles that are associated with the console—`stdin`, `stdout`, and `stderr`—must be redirected before C run-time functions can use them in [!INCLUDE[win8_appname_long](../vs140/includes/win8_appname_long_md.md)] apps. For additional compatibility information, see [Compatibility](../vs140/Compatibility.md).  
  
## Example  
  
```  
// crt_vscanf.c  
// compile with: /W3  
// This program uses the vscanf and vwscanf functions  
// to read formatted input.  
  
#include <stdio.h>  
#include <stdarg.h>  
  
int call_vscanf(char *format, ...)  
{  
    int result;  
    va_list arglist;  
    va_start(arglist, format);  
    result = vscanf(format, arglist);  
    va_end(arglist);  
    return result;  
}  
  
int call_vwscanf(wchar_t *format, ...)  
{  
    int result;  
    va_list arglist;  
    va_start(arglist, format);  
    result = vwscanf(format, arglist);  
    va_end(arglist);  
    return result;  
}  
  
int main( void )  
{  
    int   i, result;  
    float fp;  
    char  c, s[81];  
    wchar_t wc, ws[81];  
    result = call_vscanf( "%d %f %c %C %80s %80S", &i, &fp, &c, &wc, s, ws );  
    printf( "The number of fields input is %d\n", result );  
    printf( "The contents are: %d %f %c %C %s %S\n", i, fp, c, wc, s, ws);  
    result = call_vwscanf( L"%d %f %hc %lc %80S %80ls", &i, &fp, &c, &wc, s, ws );  
    wprintf( L"The number of fields input is %d\n", result );  
    wprintf( L"The contents are: %d %f %C %c %hs %s\n", i, fp, c, wc, s, ws);  
}  
  
```  
  
  **`71 98.6 h z Byte characters 36 92.3 y n Wide characters`The number of fields input is 6**  
**The contents are: 71 98.599998 h z Byte characters**  
**The number of fields input is 6**  
**The contents are: 36 92.300003 y n Wide characters**   
## .NET Framework Equivalent  
  
-   [System::Console::Read](https://msdn.microsoft.com/en-us/library/system.console.read.aspx)  
  
-   [System::Console::ReadLine](https://msdn.microsoft.com/en-us/library/system.console.readline.aspx)  
  
-   See also `Parse` methods, such as [System::Double::Parse](https://msdn.microsoft.com/en-us/library/system.double.parse.aspx).  
  
## See Also  
 [Floating-Point Support](../vs140/Floating-Point-Support.md)   
 [Stream I/O](../vs140/Stream-I-O.md)   
 [Locale](../vs140/Locale.md)   
 [fscanf, _fscanf_l, fwscanf, _fwscanf_l](../vs140/fscanf--_fscanf_l--fwscanf--_fwscanf_l.md)   
 [printf, _printf_l, wprintf, _wprintf_l](../vs140/printf--_printf_l--wprintf--_wprintf_l.md)   
 [sprintf, _sprintf_l, swprintf, _swprintf_l, \__swprintf_l](../vs140/sprintf--_sprintf_l--swprintf--_swprintf_l--__swprintf_l.md)   
 [sscanf, _sscanf_l, swscanf, _swscanf_l](../vs140/sscanf--_sscanf_l--swscanf--_swscanf_l.md)   
 [vscanf_s, vwscanf_s](../vs140/vscanf_s--vwscanf_s.md)