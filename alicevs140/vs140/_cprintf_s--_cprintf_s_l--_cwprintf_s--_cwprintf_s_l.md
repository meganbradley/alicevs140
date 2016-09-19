---
title: "_cprintf_s, _cprintf_s_l, _cwprintf_s, _cwprintf_s_l"
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
  - _cwprintf_s_l
  - _cprintf_s_l
  - _cprintf_s
  - _cwprintf_s
apilocation: 
  - msvcr80.dll
  - msvcr120.dll
  - msvcr110.dll
  - msvcr110_clr0400.dll
  - msvcr90.dll
  - msvcrt.dll
  - msvcr100.dll
apitype: DLLExport
ms.assetid: c28504fe-0d20-4f06-8f97-ee33225922ad
caps.latest.revision: 28
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _cprintf_s, _cprintf_s_l, _cwprintf_s, _cwprintf_s_l
Formats and prints to the console. These versions of [_cprintf, _cprintf_l, _cwprintf, _cwprintf_l](../vs140/_cprintf--_cprintf_l--_cwprintf--_cwprintf_l.md) have security enhancements, as described in [Security Enhancements in the CRT](../vs140/Security-Features-in-the-CRT.md).  
  
> [!IMPORTANT]
>  This API cannot be used in applications that execute in the Windows Runtime. For more information, see [CRT functions not supported with /ZW](http://msdn.microsoft.com/library/windows/apps/jj606124.aspx).  
  
## Syntax  
  
```  
int _cprintf_s(   
   const char * format [,   
   argument] ...   
);  
int _cprintf_s_l(   
   const char * format,  
   locale_t locale [,   
   argument] ...   
);  
int _cwprintf_s(  
   const wchar * format [,   
   argument] ...  
);  
int _cwprintf_s_l(  
   const wchar * format,  
   locale_t locale [,   
   argument] ...  
);  
```  
  
#### Parameters  
 `format`  
 Format-control string.  
  
 `argument`  
 Optional parameters.  
  
 `locale`  
 The locale to use.  
  
## Return Value  
 The number of characters printed.  
  
## Remarks  
 These functions format and print a series of characters and values directly to the console, using the `_putch` function (`_putwch` for `_cwprintf_s`) to output characters. Each `argument` (if any) is converted and output according to the corresponding format specification in `format`. The format has the same form and function as the `format` parameter for the [printf_s](../vs140/Format-Specification-Syntax--printf-and-wprintf-Functions.md) function. Unlike the `fprintf_s`, `printf_s`, and `sprintf_s` functions, neither `_cprintf_s` nor `_cwprintf_s` translates line-feed characters into carriage return–line feed (CR-LF) combinations when output.  
  
 An important distinction is that `_cwprintf_s` displays Unicode characters when used in Windows NT. Unlike `_cprintf_s`, `_cwprintf_s` uses the current console locale  
  
 The versions of these functions with the `_l` suffix are identical except that they use the locale parameter passed in instead of the current locale.  
  
> [!IMPORTANT]
>  Ensure that `format` is not a user-defined string.  
  
 Like the non-secure versions (see [_cprintf, _cwprintf](../vs140/_cprintf--_cprintf_l--_cwprintf--_cwprintf_l.md)), these functions validate their parameters and invoke the invalid parameter handler, as described in [Parameter Validation](../vs140/Parameter-Validation.md), if `format` is a null pointer. These functions differ from the non-secure versions in that the format string itself is also validated. If there are any unknown or badly formed formatting specifiers, these functions invoke the invalid parameter handler. In all cases, If execution is allowed to continue, the functions return -1 and set `errno` to `EINVAL`.  
  
### Generic-Text Routine Mappings  
  
|Tchar.h routine|_UNICODE and _MBCS not defined|_MBCS defined|_UNICODE defined|  
|---------------------|--------------------------------------|--------------------|-----------------------|  
|`_tcprintf_s`|`_cprintf_s`|`_cprintf_s`|`_cwprintf_s`|  
|`_tcprintf_s_l`|`_cprintf_s_l`|`_cprintf_s_l`|`_cwprintf_s_l`|  
  
## Requirements  
  
|Routine|Required header|  
|-------------|---------------------|  
|`_cprintf_s`,`_cprintf_s_l`|<conio.h>|  
|`_cwprintf_s`, `_cwprintf_s_l`|<conio.h>|  
  
 For more compatibility information, see [Compatibility](../vs140/Compatibility.md).  
  
## Libraries  
 All versions of the [C run-time libraries](../vs140/CRT-Library-Features.md).  
  
## Example  
  
```  
// crt_cprintf_s.c  
// compile with: /c  
// This program displays some variables to the console.  
  
#include <conio.h>  
  
int main( void )  
{  
   int      i = -16, h = 29;  
   unsigned u = 62511;  
   char     c = 'A';  
   char     s[] = "Test";  
  
   /* Note that console output does not translate \n as  
    * standard output does. Use \r\n instead.  
    */  
   _cprintf_s( "%d  %.4x  %u  %c %s\r\n", i, h, u, c, s );  
}  
```  
  
## Output  
  
```  
-16  001d  62511  A Test  
```  
  
## See Also  
 [Console and Port I/O](../vs140/Console-and-Port-I-O.md)   
 [_cscanf, _cwscanf](../vs140/_cscanf--_cscanf_l--_cwscanf--_cwscanf_l.md)   
 [fprintf_s, fwprintf_s](../vs140/fprintf_s--_fprintf_s_l--fwprintf_s--_fwprintf_s_l.md)   
 [printf_s, wprintf_s](../vs140/printf_s--_printf_s_l--wprintf_s--_wprintf_s_l.md)   
 [sprintf_s, swprintf_s](../vs140/sprintf_s--_sprintf_s_l--swprintf_s--_swprintf_s_l.md)   
 [vfprintf_s, vfwprintf_s](../vs140/vfprintf_s--_vfprintf_s_l--vfwprintf_s--_vfwprintf_s_l.md)   
 [Format Specification Fields: printf and wprintf Functions](../vs140/Format-Specification-Syntax--printf-and-wprintf-Functions.md)