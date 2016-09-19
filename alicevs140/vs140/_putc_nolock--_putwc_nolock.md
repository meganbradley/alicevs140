---
title: "_putc_nolock, _putwc_nolock"
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
  - _putc_nolock
  - _putwc_nolock
apilocation: 
  - msvcr90.dll
  - msvcr80.dll
  - msvcr110_clr0400.dll
  - msvcr100.dll
  - msvcr120.dll
  - msvcrt.dll
  - msvcr110.dll
apitype: DLLExport
ms.assetid: 3cfc7f21-c9e8-4b7f-b0fb-af0d4d85e7e1
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _putc_nolock, _putwc_nolock
Writes a character to a stream without locking the thread.  
  
## Syntax  
  
```  
  
      int _putc_nolock(  
   int c,  
   FILE *stream   
);  
wint_t _putwc_nolock(  
   wchar_t c,  
   FILE *stream   
);  
```  
  
#### Parameters  
 `c`  
 Character to be written.  
  
 `stream`  
 Pointer to the **FILE** structure.  
  
## Return Value  
 See **putc, putwc**.  
  
## Remarks  
 `_putc_nolock` and `_putwc_nolock` are identical to the versions without the **_nolock** suffix except that they are not protected from interference by other threads. They might be faster because they do not incur the overhead of locking out other threads. Use these functions only in thread-safe contexts such as single-threaded applications or where the calling scope already handles thread isolation.  
  
 `_putwc_nolock` is the wide-character version of `_putc_nolock`; the two functions behave identically if the stream is opened in ANSI mode. `_putc_nolock` doesn't currently support output into a UNICODE stream.  
  
### Generic-Text Routine Mappings  
  
|Tchar.h routine|_UNICODE and _MBCS not defined|_MBCS defined|_UNICODE defined|  
|---------------------|--------------------------------------|--------------------|-----------------------|  
|`_puttc_nolock`|`_putc_nolock`|`_putc_nolock`|**_putwc_nolock**|  
  
## Requirements  
  
|Routine|Required header|  
|-------------|---------------------|  
|`_putc_nolock`|<stdio.h>|  
|`_putwc_nolock`|<stdio.h> or <wchar.h>|  
  
 The console is not supported in [!INCLUDE[win8_appname_long](../vs140/includes/win8_appname_long_md.md)] apps. The standard stream handles that are associated with the console—`stdin`, `stdout`, and `stderr`—must be redirected before C run-time functions can use them in [!INCLUDE[win8_appname_long](../vs140/includes/win8_appname_long_md.md)] apps. For more compatibility information, see [Compatibility](../vs140/Compatibility.md).  
  
## Libraries  
 All versions of the [C run-time libraries](../vs140/CRT-Library-Features.md).  
  
## Example  
  
```  
// crt_putc_nolock.c  
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
      ch = _putc_nolock( *p, stream );  
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