---
title: "fputc, fputwc"
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
  - fputc
  - fputwc
apilocation: 
  - msvcr80.dll
  - msvcr110_clr0400.dll
  - msvcr120.dll
  - msvcr110.dll
  - msvcrt.dll
  - msvcr100.dll
  - msvcr90.dll
apitype: DLLExport
ms.assetid: 5a0a593d-43f4-4fa2-a401-ec4e23de4d2f
caps.latest.revision: 20
translation.priority.ht: 
  - de-de
  - ja-jp
---
# fputc, fputwc
Writes a character to a stream.  
  
## Syntax  
  
```  
int fputc(  
   int c,  
   FILE *stream   
);  
wint_t fputwc(  
   wchar_t c,  
   FILE *stream   
);  
```  
  
#### Parameters  
 `c`  
 Character to be written.  
  
 `stream`  
 Pointer to `FILE` structure.  
  
## Return Value  
 Each of these functions returns the character written. For `fputc`, a return value of `EOF` indicates an error. For `fputwc`, a return value of `WEOF` indicates an error. If `stream` is `NULL`, these functions invoke the invalid parameter handler, as described in [Parameter Validation](../vs140/Parameter-Validation.md). If execution is allowed to continue, they return `EOF` and set `errno` to `EINVAL`.  
  
 See [_doserrno, errno, _sys_errlist, and _sys_nerr](../vs140/errno--_doserrno--_sys_errlist--and-_sys_nerr.md) for more information on these, and other, error codes.  
  
## Remarks  
 Each of these functions writes the single character `c` to a file at the position indicated by the associated file position indicator (if defined) and advances the indicator as appropriate. In the case of `fputc` and `fputwc`, the file is associated with `stream`*.* If the file cannot support positioning requests or was opened in append mode, the character is appended to the end of the stream.  
  
 The two functions behave identically if the stream is opened in ANSI mode. `fputc` does not currently support output into a UNICODE stream.  
  
 The versions with the `_nolock` suffix are identical except that they are not protected from interference by other threads. For more information, see[_fputc_nolock, _fputwc_nolock](../vs140/_fputc_nolock--_fputwc_nolock.md).  
  
 Routine-specific remarks follow.  
  
|Routine|Remarks|  
|-------------|-------------|  
|`fputc`|Equivalent to `putc`, but implemented only as a function, rather than as a function and a macro.|  
|`fputwc`|Wide-character version of `fputc`. Writes `c` as a multibyte character or a wide character according to whether `stream` is opened in text mode or binary mode.|  
  
### Generic-Text Routine Mappings  
  
|TCHAR.H routine|_UNICODE & _MBCS not defined|_MBCS defined|_UNICODE defined|  
|---------------------|------------------------------------|--------------------|-----------------------|  
|`_fputtc`|`fputc`|`fputc`|`fputwc`|  
  
## Requirements  
  
|Function|Required header|  
|--------------|---------------------|  
|`fputc`|<stdio.h>|  
|`fputwc`|<stdio.h> or <wchar.h>|  
  
 The console is not supported in [!INCLUDE[win8_appname_long](../vs140/includes/win8_appname_long_md.md)] apps. The standard stream handles that are associated with the console—`stdin`, `stdout`, and `stderr`—must be redirected before C run-time functions can use them in [!INCLUDE[win8_appname_long](../vs140/includes/win8_appname_long_md.md)] apps. For additional compatibility information, see [Compatibility](../vs140/Compatibility.md).  
  
## Example  
  
```  
// crt_fputc.c  
// This program uses fputc  
// to send a character array to stdout.  
  
#include <stdio.h>  
  
int main( void )  
{  
   char strptr1[] = "This is a test of fputc!!\n";  
   char *p;  
  
   // Print line to stream using fputc.   
   p = strptr1;  
   while( (*p != '\0') && fputc( *(p++), stdout ) != EOF ) ;  
  
}  
```  
  
 **This is a test of fputc!!**   
## .NET Framework Equivalent  
  
-   [System::IO::StreamWriter::Write](https://msdn.microsoft.com/en-us/library/system.io.streamwriter.write.aspx)  
  
-   [System::Console::Write](https://msdn.microsoft.com/en-us/library/system.console.write.aspx)  
  
## See Also  
 [Stream I/O](../vs140/Stream-I-O.md)   
 [fgetc, fgetwc](../vs140/fgetc--fgetwc.md)   
 [putc, putwc](../vs140/putc--putwc.md)