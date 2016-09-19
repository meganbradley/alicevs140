---
title: "_vfprintf_p, _vfprintf_p_l, _vfwprintf_p, _vfwprintf_p_l"
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
  - _vfprintf_p
  - _vfwprintf_p
  - _vfprintf_p_l
  - _vfwprintf_p_l
apilocation: 
  - msvcr110.dll
  - msvcr100.dll
  - msvcr120.dll
  - msvcr90.dll
  - msvcr110_clr0400.dll
  - msvcrt.dll
  - msvcr80.dll
apitype: DLLExport
ms.assetid: 4d4a0914-4175-4b65-9ca1-037c4ef29147
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _vfprintf_p, _vfprintf_p_l, _vfwprintf_p, _vfwprintf_p_l
Write formatted output using a pointer to a list of arguments, with the ability to specify the order that arguments are used in the format string.  
  
## Syntax  
  
```  
int _vfprintf_p(  
   FILE *stream,  
   const char *format,  
   va_list argptr   
);  
int _vfprintf_p_l(  
   FILE *stream,  
   const char *format,  
   locale_t locale,  
   va_list argptr   
);  
int _vfwprintf_p(  
   FILE *stream,  
   const wchar_t *format,  
   va_list argptr   
);  
int _vfwprintf_p_l(  
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
 `_vfprintf_p` and `_vfwprintf_p` return the number of characters written, not including the terminating null character, or a negative value if an output error occurs.  
  
## Remarks  
 Each of these functions takes a pointer to an argument list, then formats and writes the given data to `stream`. These functions differ from the `_vfprint_s` and `_vfwprint_s` versions only in that they support positional parameters. For more information, see [printf Positional Parameters](../vs140/printf_p-Positional-Parameters.md).  
  
 `_vfwprintf_p` is the wide-character version of `_vprintf_p`; the two functions behave identically if the stream is opened in ANSI mode. `_vprintf_p` doesn't currently support output into a UNICODE stream.  
  
 The versions of these functions with the `_l` suffix are identical except that they use the locale parameter passed in instead of the current thread locale.  
  
> [!IMPORTANT]
>  Ensure that `format` is not a user-defined string. For more information, see [Avoiding Buffer Overruns](http://msdn.microsoft.com/library/windows/desktop/ms717795).  
  
 If either `stream` or `format` is a null pointer, or if the format string contains invalid formatting characters, the invalid parameter handler is invoked, as described in [Parameter Validation](../vs140/Parameter-Validation.md). If execution is allowed to continue, the functions return -1 and set `errno` to `EINVAL`.  
  
### Generic-Text Routine Mappings  
  
|TCHAR.H routine|_UNICODE & _MBCS not defined|_MBCS defined|_UNICODE defined|  
|---------------------|------------------------------------|--------------------|-----------------------|  
|`_vftprintf_p`|`_vfprintf_p`|`_vfprintf_p`|`_vfwprintf_p`|  
|`_vftprintf_p_l`|`_vfprintf_p_l`|`_vfprintf_p_l`|`_vfwprintf_p_l`|  
  
## Requirements  
  
|Routine|Required header|Optional headers|  
|-------------|---------------------|----------------------|  
|`_vfprintf_p`, `_vfprintf_p_l`|<stdio.h> and <stdarg.h>|<varargs.h>*|  
|`_vfwprintf_p`, `_vfwprintf_p_l`|<stdio.h> or <wchar.h>, and <stdarg.h>|<varargs.h>*|  
  
 \* Required for UNIX V compatibility.  
  
 For additional compatibility information, see [Compatibility](../vs140/Compatibility.md) in the Introduction.  
  
## .NET Framework Equivalent  
 Not applicable. To call the standard C function, use `PInvoke`. For more information, see [Platform Invoke Examples](assetId:///15926806-f0b7-487e-93a6-4e9367ec689f).  
  
## See Also  
 [Stream I/O](../vs140/Stream-I-O.md)   
 [vprintf Functions](../vs140/vprintf-Functions.md)   
 [fprintf, fwprintf](../vs140/fprintf--_fprintf_l--fwprintf--_fwprintf_l.md)   
 [printf, wprintf](../vs140/printf--_printf_l--wprintf--_wprintf_l.md)   
 [sprintf, swprintf](../vs140/sprintf--_sprintf_l--swprintf--_swprintf_l--__swprintf_l.md)   
 [va_arg, va_end, va_start](../vs140/va_arg--va_copy--va_end--va_start.md)   
 [printf Positional Parameters](../vs140/printf_p-Positional-Parameters.md)   
 [_fprintf_p, _fwprintf_p](../vs140/_fprintf_p--_fprintf_p_l--_fwprintf_p--_fwprintf_p_l.md)   
 [_vsprintf_p, _vswprintf_p](../vs140/_vsprintf_p--_vsprintf_p_l--_vswprintf_p--_vswprintf_p_l.md)   
 [_sprintf_p, _swprintf_p](../vs140/_sprintf_p--_sprintf_p_l--_swprintf_p--_swprintf_p_l.md)