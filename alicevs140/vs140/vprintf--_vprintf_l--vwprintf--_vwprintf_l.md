---
title: "vprintf, _vprintf_l, vwprintf, _vwprintf_l"
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
  - vprintf
  - _vwprintf_l
  - _vprintf_l
  - vwprintf
apilocation: 
  - msvcr110.dll
  - msvcr90.dll
  - msvcr120.dll
  - msvcr110_clr0400.dll
  - msvcr80.dll
  - msvcr100.dll
  - msvcrt.dll
apitype: DLLExport
ms.assetid: 44549505-00a0-4fa7-9a85-f2e666f55a38
caps.latest.revision: 22
translation.priority.ht: 
  - de-de
  - ja-jp
---
# vprintf, _vprintf_l, vwprintf, _vwprintf_l
Writes formatted output by using a pointer to a list of arguments. More secure versions of these functions are available, see [vprintf_s, _vprintf_s_l, vwprintf_s, _vwprintf_s_l](../vs140/vprintf_s--_vprintf_s_l--vwprintf_s--_vwprintf_s_l.md).  
  
## Syntax  
  
```  
int vprintf(  
   const char *format,  
   va_list argptr   
);  
int _vprintf_l(  
   const char *format,  
   locale_t locale,  
   va_list argptr   
);  
int vwprintf(  
   const wchar_t *format,  
   va_list argptr   
);  
int _vwprintf_l(  
   const wchar_t *format,  
   locale_t locale,  
   va_list argptr   
);  
```  
  
#### Parameters  
 `format`  
 Format specification.  
  
 `argptr`  
 Pointer to list of arguments.  
  
 `locale`  
 The locale to use.  
  
 For more information, see [Format Specifications](../vs140/Format-Specification-Syntax--printf-and-wprintf-Functions.md).  
  
## Return Value  
 `vprintf` and `vwprintf` return the number of characters written, not including the terminating null character, or a negative value if an output error occurs. If `format` is a null pointer, or if the format string contains invalid formatting characters, the invalid parameter handler is invoked, as described in [Parameter Validation](../vs140/Parameter-Validation.md). If execution is allowed to continue, the functions return -1 and set `errno` to `EINVAL`.  
  
 For information on these and other error codes, see [_doserrno, errno, _sys_errlist, and _sys_nerr](../vs140/errno--_doserrno--_sys_errlist--and-_sys_nerr.md).  
  
## Remarks  
 Each of these functions takes a pointer to an argument list, then formats and writes the given data to `stdout`.  
  
 `vwprintf` is the wide-character version of `vprintf`; the two functions behave identically if the stream is opened in ANSI mode. `vprintf` doesn't currently support output into a UNICODE stream.  
  
 The versions of these functions with the `_l` suffix are identical except that they use the locale parameter passed in instead of the current thread locale.  
  
> [!IMPORTANT]
>  Ensure that `format` is not a user-defined string. For more information, see [Avoiding Buffer Overruns](http://msdn.microsoft.com/library/windows/desktop/ms717795). Note that invalid format strings are detected and result in an error.  
  
### Generic-Text Routine Mappings  
  
|TCHAR.H routine|_UNICODE & _MBCS not defined|_MBCS defined|_UNICODE defined|  
|---------------------|------------------------------------|--------------------|-----------------------|  
|`_vtprintf`|`vprintf`|`vprintf`|`vwprintf`|  
|`_vtprintf_l`|`_vprintf_l`|`_vprintf_l`|`_vwprintf_l`|  
  
## Requirements  
  
|Routine|Required header|Optional headers|  
|-------------|---------------------|----------------------|  
|`vprintf`, `_vprintf_l`|<stdio.h> and <stdarg.h>|<varargs.h>*|  
|`vwprintf`, `_vwprintf_l`|<stdio.h> or <wchar.h>, and <stdarg.h>|<varargs.h>*|  
  
 \* Required for UNIX V compatibility.  
  
 The console is not supported in [!INCLUDE[win8_appname_long](../vs140/includes/win8_appname_long_md.md)] apps. The standard stream handles that are associated with the console—`stdin`, `stdout`, and `stderr`—must be redirected before C run-time functions can use them in [!INCLUDE[win8_appname_long](../vs140/includes/win8_appname_long_md.md)] apps. For additional compatibility information, see [Compatibility](../vs140/Compatibility.md).  
  
## .NET Framework Equivalent  
 [System::Console::Write](https://msdn.microsoft.com/en-us/library/system.console.write.aspx)  
  
## See Also  
 [Stream I/O](../vs140/Stream-I-O.md)   
 [vprintf Functions](../vs140/vprintf-Functions.md)   
 [fprintf, _fprintf_l, fwprintf, _fwprintf_l](../vs140/fprintf--_fprintf_l--fwprintf--_fwprintf_l.md)   
 [printf, _printf_l, wprintf, _wprintf_l](../vs140/printf--_printf_l--wprintf--_wprintf_l.md)   
 [sprintf, _sprintf_l, swprintf, _swprintf_l, \__swprintf_l](../vs140/sprintf--_sprintf_l--swprintf--_swprintf_l--__swprintf_l.md)   
 [va_arg, va_copy, va_end, va_start](../vs140/va_arg--va_copy--va_end--va_start.md)