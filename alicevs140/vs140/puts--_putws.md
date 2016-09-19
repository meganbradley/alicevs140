---
title: "puts, _putws"
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
  - _putws
  - puts
apilocation: 
  - msvcrt.dll
  - msvcr80.dll
  - msvcr110.dll
  - msvcr120.dll
  - msvcr90.dll
  - msvcr100.dll
  - msvcr110_clr0400.dll
apitype: DLLExport
ms.assetid: 32dada12-ed45-40ac-be06-3feeced9ecd6
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# puts, _putws
Writes a string to **stdout**.  
  
## Syntax  
  
```  
  
      int puts(  
   const char *str   
);  
int _putws(  
   const wchar_t *str   
);  
```  
  
#### Parameters  
 `str`  
 Output string.  
  
## Return Value  
 Returns a nonnegative value if successful. If `puts` fails, it returns `EOF`; if `_putws` fails, it returns **WEOF**. If `str` is a null pointer, the invalid parameter handler is invoked, as described in [Parameter Validation](../vs140/Parameter-Validation.md). If execution is allowed to continue, the functions set `errno` to `EINVAL` and return `EOF` or **WEOF**.  
  
 For information on these and other error codes, see [_doserrno, errno, _sys_errlist, and _sys_nerr](../vs140/errno--_doserrno--_sys_errlist--and-_sys_nerr.md).  
  
## Remarks  
 The `puts` function writes `str` to the standard output stream **stdout**, replacing the string's terminating null character ('\0') with a newline character ('\n') in the output stream.  
  
 `_putws` is the wide-character version of `puts`; the two functions behave identically if the stream is opened in ANSI mode. `puts` doesn't currently support output into a UNICODE stream.  
  
 Under Windows 2000 and later, **_putwch** writes Unicode characters using the current CONSOLE LOCALE setting.  
  
### Generic-Text Routine Mappings  
  
|TCHAR.H routine|_UNICODE & _MBCS not defined|_MBCS defined|_UNICODE defined|  
|---------------------|------------------------------------|--------------------|-----------------------|  
|`_putts`|`puts`|`puts`|`_putws`|  
  
## Requirements  
  
|Routine|Required header|  
|-------------|---------------------|  
|`puts`|<stdio.h>|  
|`_putws`|<stdio.h>|  
  
 The console is not supported in [!INCLUDE[win8_appname_long](../vs140/includes/win8_appname_long_md.md)] apps. The standard stream handles that are associated with the console—`stdin`, `stdout`, and `stderr`—must be redirected before C run-time functions can use them in [!INCLUDE[win8_appname_long](../vs140/includes/win8_appname_long_md.md)] apps. For additional compatibility information, see [Compatibility](../vs140/Compatibility.md).  
  
## Libraries  
 All versions of the [C run-time libraries](../vs140/CRT-Library-Features.md).  
  
## Example  
  
```  
// crt_puts.c  
/* This program uses puts to write a string to stdout.  
 */  
  
#include <stdio.h>  
  
int main( void )  
{  
   puts( "Hello world from puts!" );  
}  
```  
  
## Output  
  
```  
Hello world from puts!  
```  
  
## .NET Framework Equivalent  
 [System::Console::Write](https://msdn.microsoft.com/en-us/library/system.console.write.aspx)  
  
## See Also  
 [Stream I/O](../vs140/Stream-I-O.md)   
 [fputs, fputws](../vs140/fputs--fputws.md)   
 [fgets, fgetws](../vs140/fgets--fgetws.md)