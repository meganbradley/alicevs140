---
title: "vsscanf, vswscanf"
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
  - vsscanf
  - vswscanf
apilocation: 
  - msvcr110_clr0400.dll
  - msvcr110.dll
  - msvcrt.dll
  - msvcr80.dll
  - msvcr120.dll
  - msvcr90.dll
  - msvcr100.dll
apitype: DLLExport
ms.assetid: e96180f2-df46-423d-b4eb-0a49ab819bde
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# vsscanf, vswscanf
Reads formatted data from a string. More secure versions of these functions are available; see [vsscanf_s, vswscanf_s](../vs140/vsscanf_s--vswscanf_s.md).  
  
## Syntax  
  
```  
int vsscanf(  
   const char *buffer,  
   const char *format,  
   va_list arglist  
);  
int vswscanf(  
   const wchar_t *buffer,  
   const wchar_t *format,  
   va_list arglist  
);  
```  
  
#### Parameters  
 `buffer`  
 Stored data  
  
 `format`  
 Format-control string. For more information, see [Format Specification Fields: scanf and wscanf Functions](../vs140/Format-Specification-Fields--scanf-and-wscanf-Functions.md).  
  
 `arglist`  
 Variable argument list.  
  
## Return Value  
 Each of these functions returns the number of fields that are successfully converted and assigned; the return value does not include fields that were read but not assigned. A return value of 0 indicates that no fields were assigned. The return value is `EOF` for an error or if the end of the string is reached before the first conversion.  
  
 If `buffer` or `format` is a `NULL` pointer, the invalid parameter handler is invoked, as described in [Parameter Validation](../vs140/Parameter-Validation.md). If execution is allowed to continue, these functions return -1 and set `errno` to `EINVAL`.  
  
 For information about these and other error codes, see [errno, _doserrno, _sys_errlist, and _sys_nerr](../vs140/errno--_doserrno--_sys_errlist--and-_sys_nerr.md).  
  
## Remarks  
 The `vsscanf` function reads data from `buffer` into the locations that are given by each argument in the `arglist` argument list. Every argument in the list must be a pointer to a variable that has a type that corresponds to a type specifier in `format`. The `format` argument controls the interpretation of the input fields and has the same form and function as the `format` argument for the `scanf` function. If copying takes place between strings that overlap, the behavior is undefined.  
  
> [!IMPORTANT]
>  When you use `vsscanf` to read a string, always specify a width for the `%s` format (for example, `"%32s"` instead of `"%s"`); otherwise, incorrectly formatted input can cause a buffer overrun.  
  
 `vswscanf` is a wide-character version of `vsscanf`; the arguments to `vswscanf` are wide-character strings. `vsscanf` does not handle multibyte hexadecimal characters. `vswscanf` does not handle Unicode full-width hexadecimal or "compatibility zone" characters. Otherwise, `vswscanf` and `vsscanf` behave identically.  
  
### Generic-Text Routine Mappings  
  
|TCHAR.H routine|_UNICODE & _MBCS not defined|_MBCS defined|_UNICODE defined|  
|---------------------|------------------------------------|--------------------|-----------------------|  
|`_vstscanf`|`vsscanf`|`vsscanf`|`vswscanf`|  
  
## Requirements  
  
|Routine|Required header|  
|-------------|---------------------|  
|`vsscanf`|<stdio.h>|  
|`vswscanf`|<stdio.h> or <wchar.h>|  
  
 For additional compatibility information, see [Compatibility](../vs140/Compatibility.md).  
  
## Example  
  
```  
// crt_vsscanf.c  
// compile with: /W3  
// This program uses vsscanf to read data items  
// from a string named tokenstring, then displays them.  
  
#include <stdio.h>  
#include <stdarg.h>  
  
int call_vsscanf(char *tokenstring, char *format, ...)  
{  
    int result;  
    va_list arglist;  
    va_start(arglist, format);  
    result = vsscanf(tokenstring, format, arglist);  
    va_end(arglist);  
    return result;  
}  
  
int main( void )  
{  
    char  tokenstring[] = "15 12 14...";  
    char  s[81];  
    char  c;  
    int   i;  
    float fp;  
  
    // Input various data from tokenstring:  
    // max 80 character string:  
    call_vsscanf(tokenstring, "%80s", s);  
    call_vsscanf(tokenstring, "%c", &c);  
    call_vsscanf(tokenstring, "%d", &i);  
    call_vsscanf(tokenstring, "%f", &fp);  
  
    // Output the data read  
    printf("String    = %s\n", s);  
    printf("Character = %c\n", c);  
    printf("Integer:  = %d\n", i);  
    printf("Real:     = %f\n", fp);  
}  
```  
  
 **String    = 15**  
**Character = 1**  
**Integer:  = 15**  
**Real:     = 15.000000**   
## .NET Framework Equivalent  
 See `Parse` methods, such as [System::Double::Parse](https://msdn.microsoft.com/en-us/library/system.double.parse.aspx).  
  
## See Also  
 [Stream I/O](../vs140/Stream-I-O.md)   
 [scanf, wscanf](../vs140/scanf--_scanf_l--wscanf--_wscanf_l.md)   
 [sscanf, swscanf](../vs140/sscanf--_sscanf_l--swscanf--_swscanf_l.md)   
 [sprintf, swprintf](../vs140/sprintf--_sprintf_l--swprintf--_swprintf_l--__swprintf_l.md)   
 [vsscanf_s, vswscanf_s](../vs140/vsscanf_s--vswscanf_s.md)