---
title: "vfprintf_s, _vfprintf_s_l, vfwprintf_s, _vfwprintf_s_l"
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
  - vfwprintf_s
  - _vfprintf_s_l
  - vfprintf_s
  - _vfwprintf_s_l
apilocation: 
  - msvcr110.dll
  - msvcr120.dll
  - msvcr80.dll
  - msvcrt.dll
  - msvcr110_clr0400.dll
  - msvcr100.dll
  - msvcr90.dll
apitype: DLLExport
ms.assetid: eab6f563-46e2-4806-963f-2b23f339ecdc
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# vfprintf_s, _vfprintf_s_l, vfwprintf_s, _vfwprintf_s_l
Write formatted output using a pointer to a list of arguments. These are versions of [vfprintf, _vfprintf_l, vfwprintf, _vfwprintf_l](../vs140/vfprintf--_vfprintf_l--vfwprintf--_vfwprintf_l.md) with security enhancements as described in [Security Enhancements in the CRT](../vs140/Security-Features-in-the-CRT.md).  
  
## Syntax  
  
```  
int vfprintf_s(  
   FILE *stream,  
   const char *format,  
   va_list argptr   
);  
int _vfprintf_s_l(  
   FILE *stream,  
   const char *format,  
   locale_t locale,  
   va_list argptr   
);  
int vfwprintf_s(  
   FILE *stream,  
   const wchar_t *format,  
   va_list argptr   
);  
int _vfwprintf_s_l(  
   FILE *stream,  
   const wchar_t *format,  
   locale_t locale,  
   va_list argptr   
);  
```  
  
#### Parameters  
 `stream`  
 Pointer to `FILE` structure.  
  
 `format`  
 Format specification.  
  
 `argptr`  
 Pointer to list of arguments.  
  
 `locale`  
 The locale to use.  
  
 For more information, see [Format Specifications](../vs140/Format-Specification-Syntax--printf-and-wprintf-Functions.md).  
  
## Return Value  
 `vfprintf_s` and `vfwprintf_s` return the number of characters written, not including the terminating null character, or a negative value if an output error occurs. If either `stream` or `format` is a null pointer, or if the format string contains invalid formatting characters, the invalid parameter handler is invoked, as described in [Parameter Validation](../vs140/Parameter-Validation.md). If execution is allowed to continue, the functions return -1 and set `errno` to `EINVAL`.  
  
 For information on these and other error codes, see [_doserrno, errno, _sys_errlist, and _sys_nerr](../vs140/errno--_doserrno--_sys_errlist--and-_sys_nerr.md).  
  
## Remarks  
 Each of these functions takes a pointer to an argument list, then formats and writes the given data to `stream`.  
  
 These functions differ from the non-secure versions only in that the secure versions check that the `format` string contains valid formatting characters.  
  
 `vfwprintf_s` is the wide-character version of `vfprintf_s`; the two functions behave identically if the stream is opened in ANSI mode. `vfprintf_s` doesn't currently support output into a UNICODE stream.  
  
 The versions of these functions with the `_l` suffix are identical except that they use the locale parameter passed in instead of the current thread locale.  
  
> [!IMPORTANT]
>  Ensure that `format` is not a user-defined string. For more information, see [Avoiding Buffer Overruns](http://msdn.microsoft.com/library/windows/desktop/ms717795).  
  
### Generic-Text Routine Mappings  
  
|TCHAR.H routine|_UNICODE & _MBCS not defined|_MBCS defined|_UNICODE defined|  
|---------------------|------------------------------------|--------------------|-----------------------|  
|`_vftprintf_s`|`vfprintf_s`|`vfprintf_s`|`vfwprintf_s`|  
|`_vftprintf_s_l`|`_vfprintf_s_l`|`_vfprintf_s_l`|`_vfwprintf_s_l`|  
  
## Requirements  
  
|Routine|Required header|Optional headers|  
|-------------|---------------------|----------------------|  
|`vfprintf_s`, _`vfprintf_s_l`|<stdio.h> and <stdarg.h>|<varargs.h>*|  
|`vfwprintf_s`, _`vfwprintf_s_l`|<stdio.h> or <wchar.h>, and <stdarg.h>|<varargs.h>*|  
  
 \* Required for UNIX V compatibility.  
  
 For additional compatibility information, see [Compatibility](../vs140/Compatibility.md) in the Introduction.  
  
## .NET Framework Equivalent  
 Not applicable. To call the standard C function, use `PInvoke`. For more information, see [Platform Invoke Examples](assetId:///15926806-f0b7-487e-93a6-4e9367ec689f).  
  
## See Also  
 [Stream I/O](../vs140/Stream-I-O.md)   
 [vprintf Functions](../vs140/vprintf-Functions.md)   
 [fprintf, _fprintf_l, fwprintf, _fwprintf_l](../vs140/fprintf--_fprintf_l--fwprintf--_fwprintf_l.md)   
 [printf, _printf_l, wprintf, _wprintf_l](../vs140/printf--_printf_l--wprintf--_wprintf_l.md)   
 [sprintf, _sprintf_l, swprintf, _swprintf_l, \__swprintf_l](../vs140/sprintf--_sprintf_l--swprintf--_swprintf_l--__swprintf_l.md)   
 [va_arg, va_copy, va_end, va_start](../vs140/va_arg--va_copy--va_end--va_start.md)