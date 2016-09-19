---
title: "_vcprintf_p, _vcprintf_p_l, _vcwprintf_p, _vcwprintf_p_l"
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
  - _vcprintf_p
  - _vcwprintf_p_l
  - _vcprintf_p_l
  - _vcwprintf_p
apilocation: 
  - msvcr120.dll
  - msvcr90.dll
  - msvcrt.dll
  - msvcr80.dll
  - msvcr100.dll
  - msvcr110_clr0400.dll
  - msvcr110.dll
apitype: DLLExport
ms.assetid: 611024cc-90e7-41db-8e85-145ca95012b1
caps.latest.revision: 20
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _vcprintf_p, _vcprintf_p_l, _vcwprintf_p, _vcwprintf_p_l
Writes formatted output to the console by using a pointer to a list of arguments, and supports positional parameters in the format string.  
  
> [!IMPORTANT]
>  This API cannot be used in applications that execute in the [!INCLUDE[wrt](../vs140/includes/wrt_md.md)]. For more information, see [CRT functions not supported with /ZW](http://msdn.microsoft.com/library/windows/apps/jj606124.aspx).  
  
## Syntax  
  
```  
int _vcprintf_p(  
   const char* format,  
   va_list argptr  
);  
int _vcprintf_p_l(  
   const char* format,  
   locale_t locale,  
   va_list argptr  
);  
int _vcwprintf_p(  
   const wchar_t* format,  
   va_list argptr  
);  
int _vcwprintf_p_l(  
   const wchar_t* format,  
   locale_t locale,  
   va_list argptr  
);  
```  
  
#### Parameters  
 `format`  
 The format specification.  
  
 `argptr`  
 A pointer to a list of arguments.  
  
 `locale`  
 The locale to use.  
  
 For more information, see [Format Specification Syntax: printf and wprintf Functions](../vs140/Format-Specification-Syntax--printf-and-wprintf-Functions.md).  
  
## Return Value  
 The number of characters that are written, or a negative value if an output error occurs. If `format` is a null pointer, the invalid parameter handler is invoked, as described in [Parameter Validation](../vs140/Parameter-Validation.md). If execution is allowed to continue, `errno` is set to `EINVAL` and -1 is returned.  
  
## Remarks  
 Each of these functions takes a pointer to an argument list, and then uses the `_putch` function to format and write the given data to the console. (`_vcwprintf_p` uses `_putwch` instead of `_putch`. `_vcwprintf_p` is the wide-character version of `_vcprintf_p`. It takes a wide-character string as an argument.)  
  
 The versions of these functions that have the `_l` suffix are identical except that they use the locale parameter that's passed in instead of the current locale.  
  
 Each `argument` (if any) is converted and is output according to the corresponding format specification in `format`. The format specification supports positional parameters so that you can specify the order in which the arguments are used in the format string. For more information, see [printf Positional Parameters](../vs140/printf_p-Positional-Parameters.md).  
  
 These functions do not translate line-feed characters into carriage return-line feed (CR-LF) combinations when they are output.  
  
> [!IMPORTANT]
>  Ensure that `format` is not a user-defined string. For more information, see [Avoiding Buffer Overruns](http://msdn.microsoft.com/library/windows/desktop/ms717795).  
  
 These functions validate the input pointer and the format string. If `format` or `argument` is `NULL`, or if the format string contains invalid formatting characters, these functions invoke the invalid parameter handler, as described in [Parameter Validation](../vs140/Parameter-Validation.md). If execution is allowed to continue, these functions return -1 and set `errno` to `EINVAL`.  
  
### Generic-Text Routine Mappings  
  
|Tchar.h routine|_UNICODE and _MBCS not defined|_MBCS defined|_UNICODE defined|  
|---------------------|--------------------------------------|--------------------|-----------------------|  
|`_vtcprintf_p`|`_vcprintf_p`|`_vcprintf_p`|`_vcwprintf_p`|  
|`_vtcprintf_p_l`|`_vcprintf_p_l`|`_vcprintf_p_l`|`_vcwprintf_p_l`|  
  
## Requirements  
  
|Routine|Required header|  
|-------------|---------------------|  
|`_vcprintf_p`, `_vcprintf_p_l`|<conio.h> and <stdarg.h>|  
|`_vcwprintf_p`, `_vcwprintf_p_l`|<conio.h> and <stdarg.h>|  
  
 For more compatibility information, see [Compatibility](../vs140/Compatibility.md).  
  
## Example  
  
```  
  
      // crt_vcprintf_p.c  
// compile with: /c  
#include <conio.h>  
#include <stdarg.h>  
  
// An error formatting function that's used to print to the console.  
int eprintf(const char* format, ...)  
{  
  va_list args;  
  va_start(args, format);  
  return _vcprintf_p(format, args);  
}  
  
int main()  
{  
   int n = eprintf("parameter 2 = %2$d; parameter 1 = %1$s\r\n",  
      "one", 222);  
   _cprintf_s("%d characters printed\r\n");  
}  
```  
  
 **parameter 2 = 222; parameter 1 = one**  
**38 characters printed**   
## See Also  
 [Console and Port I/O](../vs140/Console-and-Port-I-O.md)   
 [_cprintf, _cprintf_l, _cwprintf, _cwprintf_l](../vs140/_cprintf--_cprintf_l--_cwprintf--_cwprintf_l.md)   
 [va_arg, va_copy, va_end, va_start](../vs140/va_arg--va_copy--va_end--va_start.md)   
 [printf Positional Parameters](../vs140/printf_p-Positional-Parameters.md)