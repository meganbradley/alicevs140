---
title: "putc, putwc"
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
  - putwc
  - putc
apilocation: 
  - msvcr110_clr0400.dll
  - msvcr110.dll
  - msvcr100.dll
  - msvcr80.dll
  - msvcr90.dll
  - msvcr120.dll
  - msvcrt.dll
apitype: DLLExport
ms.assetid: a37b2e82-9d88-4565-8190-ff8d04c0ddb9
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# putc, putwc
Writes a character to a stream.  
  
## Syntax  
  
```  
  
      int putc(  
   int c,  
   FILE *stream   
);  
wint_t putwc(  
   wchar_t c,  
   FILE *stream   
);  
```  
  
#### Parameters  
 `c`  
 Character to be written.  
  
 `stream`  
 Pointer to **FILE** structure.  
  
## Return Value  
 Returns the character written. To indicate an error or end-of-file condition, `putc` and `putchar` return `EOF`; `putwc` and `putwchar` return **WEOF**. For all four routines, use [ferror](../vs140/ferror.md) or [feof](../vs140/feof.md) to check for an error or end of file. If passed a null pointer for `stream`, the invalid parameter handler is invoked, as described in [Parameter Validation](../vs140/Parameter-Validation.md). If execution is allowed to continue, these functions return `EOF` or **WEOF** and set `errno` to `EINVAL`.  
  
 See [_doserrno, errno, _sys_errlist, and _sys_nerr](../vs140/errno--_doserrno--_sys_errlist--and-_sys_nerr.md) for more information on these, and other, error codes.  
  
## Remarks  
 The `putc` routine writes the single character `c` to the output `stream` at the current position. Any integer can be passed to `putc`, but only the lower 8 bits are written. The `putchar` routine is identical to **putc(** `c`**, stdout )**. For each routine, if a read error occurs, the error indicator for the stream is set. `putc` and `putchar` are similar to `fputc` and `_fputchar`, respectively, but are implemented both as functions and as macros (see [Choosing Between Functions and Macros](../vs140/Recommendations-for-Choosing-Between-Functions-and-Macros.md)). `putwc` and `putwchar` are wide-character versions of `putc` and `putchar`, respectively. `putwc` and `putc` behave identically if the stream is opened in ANSI mode. `putc` doesn't currently support output into a UNICODE stream.  
  
 The versions with the **_nolock** suffix are identical except that they are not protected from interference by other threads. For more information, see **_putc_nolock, _putwc_nolock**.  
  
### Generic-Text Routine Mappings  
  
|TCHAR.H routine|_UNICODE & _MBCS not defined|_MBCS defined|_UNICODE defined|  
|---------------------|------------------------------------|--------------------|-----------------------|  
|`_puttc`|`putc`|`putc`|**putwc**|  
  
## Requirements  
  
|Routine|Required header|  
|-------------|---------------------|  
|`putc`|<stdio.h>|  
|`putwc`|<stdio.h> or <wchar.h>|  
  
 The console is not supported in [!INCLUDE[win8_appname_long](../vs140/includes/win8_appname_long_md.md)] apps. The standard stream handles that are associated with the console—`stdin`, `stdout`, and `stderr`—must be redirected before C run-time functions can use them in [!INCLUDE[win8_appname_long](../vs140/includes/win8_appname_long_md.md)] apps. For additional compatibility information, see [Compatibility](../vs140/Compatibility.md).  
  
## Libraries  
 All versions of the [C run-time libraries](../vs140/CRT-Library-Features.md).  
  
## Example  
  
```  
// crt_putc.c  
/* This program uses putc to write buffer  
 * to a stream. If an error occurs, the program  
 * stops before writing the entire buffer.  
 */  
  
#include <stdio.h>  
  
int main( void )  
{  
   FILE *stream;  
   char *p, buffer[] = "This is the line of output\n";  
   int  ch;  
  
   ch = 0;  
   /* Make standard out the stream and write to it. */  
   stream = stdout;  
   for( p = buffer; (ch != EOF) && (*p != '\0'); p++ )  
      ch = putc( *p, stream );  
}  
```  
  
## Output  
  
```  
This is the line of output  
```  
  
## .NET Framework Equivalent  
  
-   [System::IO::StreamWriter::Write](https://msdn.microsoft.com/en-us/library/system.io.streamwriter.write.aspx)  
  
-   [System::Console::Write](https://msdn.microsoft.com/en-us/library/system.console.write.aspx)  
  
## See Also  
 [Stream I/O](../vs140/Stream-I-O.md)   
 [fputc, fputwc](../vs140/fputc--fputwc.md)   
 [getc, getwc](../vs140/getc--getwc.md)