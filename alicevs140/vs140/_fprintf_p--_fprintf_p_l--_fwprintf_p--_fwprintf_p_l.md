---
title: "_fprintf_p, _fprintf_p_l, _fwprintf_p, _fwprintf_p_l"
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
  - _fwprintf_p
  - _fprintf_p_l
  - _fwprintf_p_l
  - _fprintf_p
apilocation: 
  - msvcr100.dll
  - msvcr110_clr0400.dll
  - msvcr90.dll
  - msvcr120.dll
  - msvcr80.dll
  - msvcrt.dll
  - msvcr110.dll
apitype: DLLExport
ms.assetid: 46b082e1-45ba-4383-9ee4-97015aa50bc6
caps.latest.revision: 20
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _fprintf_p, _fprintf_p_l, _fwprintf_p, _fwprintf_p_l
Prints formatted data to a stream.  
  
## Syntax  
  
```  
int _fprintf_p(   
   FILE *stream,  
   const char *format [,  
   argument ]...  
);  
int _fprintf_p_l(   
   FILE *stream,  
   const char *format,  
   locale_t locale [,  
   argument ]...  
);  
int _fwprintf_p(   
   FILE *stream,  
   const wchar_t *format [,  
   argument ]...  
);  
int _fwprintf_p_l(   
   FILE *stream,  
   const wchar_t *format,  
   locale_t locale [,  
   argument ]...  
);  
```  
  
#### Parameters  
 `stream`  
 Pointer to the `FILE` structure.  
  
 `format`  
 Format-control string.  
  
 `argument`  
 Optional arguments.  
  
 `locale`  
 The locale to use.  
  
## Return Value  
 `_fprintf_p` and `_fwprintf_p` return the number of characters written or return a negative value when an output error occurs.  
  
## Remarks  
 `_fprintf_p` formats and prints a series of characters and values to the output `stream`. Each function `argument` (if any) is converted and output according to the corresponding format specification in `format`. For `_fprintf_p`, the `format` argument has the same syntax and use that it has in `_printf_p`. These functions support positional parameters, meaning that the order of the parameters used by the format string can be changed. For more information about positional parameters, see [printf Positional Parameters](../vs140/printf_p-Positional-Parameters.md).  
  
 `_fwprintf_p` is a wide-character version of `_fprintf_p`; in `_fwprintf_p`, `format` is a wide-character string. These functions behave identically if the stream is opened in ANSI mode. `_fprintf_p` doesn't currently support output into a UNICODE stream.  
  
 The versions of these functions with the `_l` suffix are identical except that they use the locale parameter passed in instead of the current locale.  
  
> [!IMPORTANT]
>  Ensure that `format` is not a user-defined string.  
  
 Like the non-secure versions (see [fprintf, fwprintf](../vs140/fprintf--_fprintf_l--fwprintf--_fwprintf_l.md)), these functions validate their parameters and invoke the invalid parameter handler, as described in [Parameter Validation](../vs140/Parameter-Validation.md), if either `stream` or `format` is a null pointer or if there are any unknown or badly formed formatting specifiers. If execution is allowed to continue, the functions return -1 and set `errno` to `EINVAL`.  
  
### Generic-Text Routine Mappings  
  
|Tchar.h routine|_UNICODE and _MBCS not defined|_MBCS defined|_UNICODE defined|  
|---------------------|--------------------------------------|--------------------|-----------------------|  
|`_ftprintf_p`|`_fprintf_p`|`_fprintf_p`|`_fwprintf_p`|  
|`_ftprintf_p_l`|`_fprintf_p_l`|`_fprintf_p_l`|`_fwprintf_p_l`|  
  
 For more information, see [Format Specifications](../vs140/Format-Specification-Syntax--printf-and-wprintf-Functions.md).  
  
## Requirements  
  
|Function|Required header|  
|--------------|---------------------|  
|`_fprintf_p`, `_fprintf_p_l`|<stdio.h>|  
|`_fwprintf_p`, `_fwprintf_p_l`|<stdio.h> or <wchar.h>|  
  
 For more compatibility information, see [Compatibility](../vs140/Compatibility.md) in the Introduction.  
  
## Example  
  
```  
// crt_fprintf_p.c  
// This program uses _fprintf_p to format various  
// data and print it to the file named FPRINTF_P.OUT. It  
// then displays FPRINTF_P.OUT on the screen using the system  
// function to invoke the operating-system TYPE command.  
//   
  
#include <stdio.h>  
#include <process.h>  
  
int main( void )  
{  
    FILE    *stream = NULL;  
    int     i = 10;  
    double  fp = 1.5;  
    char    s[] = "this is a string";  
    char    c = '\n';  
  
    // Open the file  
    if ( fopen_s( &stream, "fprintf_p.out", "w" ) == 0)  
    {  
        // Format and print data  
        _fprintf_p( stream, "%2$s%1$c", c, s );  
        _fprintf_p( stream, "%d\n", i );  
        _fprintf_p( stream, "%f\n", fp );  
  
        // Close the file  
        fclose( stream );  
    }  
  
    // Verify our data  
    system( "type fprintf_p.out" );  
}  
```  
  
 **this is a string**  
**10**  
**1.500000**   
## .NET Framework Equivalent  
 [System::IO::StreamWriter::Write](https://msdn.microsoft.com/en-us/library/system.io.streamwriter.write.aspx)  
  
## See Also  
 [Stream I/O](../vs140/Stream-I-O.md)   
 [_cprintf, _cwprintf](../vs140/_cprintf--_cprintf_l--_cwprintf--_cwprintf_l.md)   
 [fscanf, fwscanf](../vs140/fscanf--_fscanf_l--fwscanf--_fwscanf_l.md)   
 [sprintf, swprintf](../vs140/sprintf--_sprintf_l--swprintf--_swprintf_l--__swprintf_l.md)   
 [printf Positional Parameters](../vs140/printf_p-Positional-Parameters.md)   
 [_cprintf_p, _cwprintf_p](../vs140/_cprintf_p--_cprintf_p_l--_cwprintf_p--_cwprintf_p_l.md)   
 [_cprintf_s, _cwprintf_s](../vs140/_cprintf_s--_cprintf_s_l--_cwprintf_s--_cwprintf_s_l.md)   
 [printf Positional Parameters](../vs140/printf_p-Positional-Parameters.md)   
 [fscanf_s, fwscanf_s](../vs140/fscanf_s--_fscanf_s_l--fwscanf_s--_fwscanf_s_l.md)