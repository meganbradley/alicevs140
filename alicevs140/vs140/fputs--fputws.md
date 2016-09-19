---
title: "fputs, fputws"
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
  - fputs
  - fputws
apilocation: 
  - msvcrt.dll
  - msvcr110.dll
  - msvcr120.dll
  - msvcr100.dll
  - msvcr90.dll
  - msvcr110_clr0400.dll
  - msvcr80.dll
apitype: DLLExport
ms.assetid: d48c82b8-aa17-4830-8c7d-30442ddbb326
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# fputs, fputws
Writes a string to a stream.  
  
## Syntax  
  
```  
int fputs(   
   const char *str,  
   FILE *stream   
);  
int fputws(   
   const wchar_t *str,  
   FILE *stream   
);  
```  
  
#### Parameters  
 `str`  
 Output string.  
  
 `stream`  
 Pointer to `FILE` structure.  
  
## Return Value  
 Each of these functions returns a nonnegative value if it is successful. On an error, `fputs` and `fputws` return `EOF`. If `str` or `stream` is a null pointer, these functions invoke the invalid parameter handler, as described in [Parameter Validation](../vs140/Parameter-Validation.md). If execution is allowed to continue, these functions set `errno` to `EINVAL` and then `fputs` returns `EOF`, and `fputws` returns `WEOF`.  
  
 See [_doserrno, errno, _sys_errlist, and _sys_nerr](../vs140/errno--_doserrno--_sys_errlist--and-_sys_nerr.md) for more information on these, and other, error codes.  
  
## Remarks  
 Each of these functions copies `str` to the output `stream` at the current position. `fputws` copies the wide-character argument `str` to `stream` as a multibyte-character string or a wide-character string according to whether `stream` is opened in text mode or binary mode, respectively. Neither function copies the terminating null character.  
  
 The two functions behave identically if the stream is opened in ANSI mode. `fputs` does not currently support output into a UNICODE stream.  
  
### Generic-Text Routine Mappings  
  
|TCHAR.H routine|_UNICODE & _MBCS not defined|_MBCS defined|_UNICODE defined|  
|---------------------|------------------------------------|--------------------|-----------------------|  
|`_fputts`|`fputs`|`fputs`|`fputws`|  
  
## Requirements  
  
|Function|Required header|  
|--------------|---------------------|  
|`fputs`|<stdio.h>|  
|`fputws`|<stdio.h> or <wchar.h>|  
  
 The console is not supported in [!INCLUDE[win8_appname_long](../vs140/includes/win8_appname_long_md.md)] apps. The standard stream handles that are associated with the console—`stdin`, `stdout`, and `stderr`—must be redirected before C run-time functions can use them in [!INCLUDE[win8_appname_long](../vs140/includes/win8_appname_long_md.md)] apps. For additional compatibility information, see [Compatibility](../vs140/Compatibility.md).  
  
## Example  
  
```  
// crt_fputs.c  
// This program uses fputs to write  
// a single line to the stdout stream.  
  
#include <stdio.h>  
  
int main( void )  
{  
   fputs( "Hello world from fputs.\n", stdout );  
}  
```  
  
 **Hello world from fputs.**   
## .NET Framework Equivalent  
 [System::IO::StreamWriter::Write](https://msdn.microsoft.com/en-us/library/system.io.streamwriter.write.aspx)  
  
## See Also  
 [Stream I/O](../vs140/Stream-I-O.md)   
 [fgets, fgetws](../vs140/fgets--fgetws.md)   
 [gets, _getws](../vs140/gets--_getws.md)   
 [puts, _putws](../vs140/puts--_putws.md)