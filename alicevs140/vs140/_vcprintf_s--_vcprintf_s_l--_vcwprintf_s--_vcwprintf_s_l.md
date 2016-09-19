---
title: "_vcprintf_s, _vcprintf_s_l, _vcwprintf_s, _vcwprintf_s_l"
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
  - _vcprintf_s
  - _vcprintf_s_l
  - _vcwprintf_s
  - _vcwprintf_s_l
apilocation: 
  - msvcr110.dll
  - msvcr90.dll
  - msvcr80.dll
  - msvcrt.dll
  - msvcr110_clr0400.dll
  - msvcr100.dll
  - msvcr120.dll
apitype: DLLExport
ms.assetid: 5a46d45a-30db-45df-9850-455cbdac5636
caps.latest.revision: 24
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _vcprintf_s, _vcprintf_s_l, _vcwprintf_s, _vcwprintf_s_l
Writes formatted output to the console by using a pointer to a list of arguments. These versions of [_vcprintf, _vcprintf_l, _vcwprintf, _vcwprintf_l](../vs140/_vcprintf--_vcprintf_l--_vcwprintf--_vcwprintf_l.md) have security enhancements, as described in [Security Enhancements in the CRT](../vs140/Security-Features-in-the-CRT.md).  
  
> [!IMPORTANT]
>  This API cannot be used in applications that execute in the Windows Runtime. For more information, see [CRT functions not supported with /ZW](http://msdn.microsoft.com/library/windows/apps/jj606124.aspx).  
  
## Syntax  
  
```  
int _vcprintf(  
   const char* format,  
   va_list argptr  
);  
int _vcprintf(  
   const char* format,  
   locale_t locale,  
   va_list argptr  
);  
int _vcwprintf_s(  
   const wchar_t* format,  
   va_list argptr  
);  
int _vcwprintf_s_l(  
   const wchar_t* format,  
   locale_t locale,  
   va_list argptr  
);  
```  
  
#### Parameters  
 `format`  
 Format specification.  
  
 `argptr`  
 Pointer to the list of arguments.  
  
 `locale`  
 The locale to use.  
  
 For more information, see [Format Specification Syntax: printf and wprintf Functions](../vs140/Format-Specification-Syntax--printf-and-wprintf-Functions.md).  
  
## Return Value  
 The number of characters written, or a negative value if an output error occurs.  
  
 Like the less secure versions of these functions, if `format` is a null pointer, the invalid parameter handler is invoked, as described in [Parameter Validation](../vs140/Parameter-Validation.md). Additionally, unlike the less secure versions of these functions, if `format` does not specify a valid format, an invalid parameter exception is generated. If execution is allowed to continue, these functions return an error code and set `errno` to that error code. The default error code is `EINVAL` if a more specific value does not apply.  
  
## Remarks  
 Each of these functions takes a pointer to an argument list, and then formats and writes the given data to the console. `_vcwprintf_s` is the wide-character version of `_vcprintf_s`. It takes a wide-character string as an argument.  
  
 The versions of these functions that have the `_l` suffix are identical except that they use the locale parameter that's passed in instead of the current locale.  
  
> [!IMPORTANT]
>  Ensure that `format` is not a user-defined string. For more information, see [Avoiding Buffer Overruns](http://msdn.microsoft.com/library/windows/desktop/ms717795).  
  
### Generic-Text Routine Mappings  
  
|TCHAR.H routine|_UNICODE & _MBCS not defined|_MBCS defined|_UNICODE defined|  
|---------------------|------------------------------------|--------------------|-----------------------|  
|`_vtcprintf_s`|`_vcprintf_s`|`_vcprintf_s`|`_vcwprintf_s`|  
|`_vtcprintf_s_l`|`_vcprintf_s_l`|`_vcprintf_s_l`|`_vcwprintf_s_l`|  
  
## Requirements  
  
|Routine|Required header|Optional headers|  
|-------------|---------------------|----------------------|  
|`_vcprintf_s`, `_vcprintf_s_l`|<conio.h> and <stdarg.h>|<varargs.h>*|  
|`_vcwprintf_s`, `_vcwprintf_s_l`|<conio.h> or <wchar.h>, and <stdarg.h>|<varargs.h>*|  
  
 \* Required for UNIX V compatibility.  
  
 For additional compatibility information, see [Compatibility](../vs140/Compatibility.md).  
  
## Example  
  
```  
// crt_vcprintf_s.cpp  
#include <conio.h>  
#include <stdarg.h>  
  
// An error formatting function used to print to the console.  
int eprintf_s(const char* format, ...)  
{  
  va_list args;  
  va_start(args, format);  
  return _vcprintf_s(format, args);  
}  
  
int main()  
{  
   eprintf_s("  (%d:%d): Error %s%d : %s\n", 10, 23, "C", 2111,  
           "<some error text>");  
   eprintf_s("  (Related to symbol '%s' defined on line %d).\n",  
           "<symbol>", 5 );  
}  
```  
  
 **(10,23): Error C2111 : <some error text\>**  
 **(Related to symbol '<symbol\>' defined on line 5).**   
## .NET Framework Equivalent  
 [System::Console::Write](https://msdn.microsoft.com/en-us/library/system.console.write.aspx)  
  
## See Also  
 [Stream I/O](../vs140/Stream-I-O.md)   
 [vprintf Functions](../vs140/vprintf-Functions.md)   
 [_cprintf, _cprintf_l, _cwprintf, _cwprintf_l](../vs140/_cprintf--_cprintf_l--_cwprintf--_cwprintf_l.md)   
 [fprintf, _fprintf_l, fwprintf, _fwprintf_l](../vs140/fprintf--_fprintf_l--fwprintf--_fwprintf_l.md)   
 [printf, _printf_l, wprintf, _wprintf_l](../vs140/printf--_printf_l--wprintf--_wprintf_l.md)   
 [sprintf, _sprintf_l, swprintf, _swprintf_l, \__swprintf_l](../vs140/sprintf--_sprintf_l--swprintf--_swprintf_l--__swprintf_l.md)   
 [va_arg, va_copy, va_end, va_start](../vs140/va_arg--va_copy--va_end--va_start.md)