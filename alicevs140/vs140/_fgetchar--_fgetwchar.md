---
title: "_fgetchar, _fgetwchar"
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
  - _fgetchar
  - _fgetwchar
apilocation: 
  - msvcr100.dll
  - msvcr120.dll
  - msvcr110_clr0400.dll
  - msvcr90.dll
  - msvcr110.dll
  - msvcrt.dll
  - msvcr80.dll
apitype: DLLExport
ms.assetid: 8bce874c-701a-41a3-b1b2-feff266fb5b9
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _fgetchar, _fgetwchar
Reads a character from `stdin`.  
  
## Syntax  
  
```  
int _fgetchar( void );  
wint_t _fgetwchar( void );  
```  
  
## Return Value  
 `_fgetchar` returns the character read as an `int` or return `EOF` to indicate an error or end of file. **_**`fgetwchar` returns, as a [wint_t](../vs140/Standard-Types.md), the wide character that corresponds to the character read or returns `WEOF` to indicate an error or end of file. For both functions, use `feof` or `ferror` to distinguish between an error and an end-of-file condition.  
  
## Remarks  
 These functions read a single character from `stdin`. The function then increments the associated file pointer (if defined) to point to the next character. If the stream is at end of file, the end-of-file indicator for the stream is set.  
  
 `_fgetchar` is equivalent to `fgetc( stdin )`. It is also equivalent to `getchar`, but implemented only as a function, rather than as a function and a macro. `_fgetwchar` is the wide-character version of `_fgetchar`.  
  
 These functions are not compatible with the ANSI standard.  
  
### Generic-Text Routine Mappings  
  
|Tchar.h routine|_UNICODE and _MBCS not defined|_MBCS defined|_UNICODE defined|  
|---------------------|--------------------------------------|--------------------|-----------------------|  
|`_fgettchar`|`_fgetchar`|`_fgetchar`|`_fgetwchar`|  
  
## Requirements  
  
|Function|Required header|  
|--------------|---------------------|  
|`_fgetchar`|<stdio.h>|  
|`_fgetwchar`|<stdio.h> or <wchar.h>|  
  
 The console is not supported in [!INCLUDE[win8_appname_long](../vs140/includes/win8_appname_long_md.md)] apps. The standard stream handles that are associated with the console—`stdin`, `stdout`, and `stderr`—must be redirected before C run-time functions can use them in [!INCLUDE[win8_appname_long](../vs140/includes/win8_appname_long_md.md)] apps. For more compatibility information, see [Compatibility](../vs140/Compatibility.md).  
  
## Example  
  
```  
// crt_fgetchar.c  
// This program uses _fgetchar to read the first  
// 80 input characters (or until the end of input)  
// and place them into a string named buffer.  
//  
  
#include <stdio.h>  
#include <stdlib.h>  
  
int main( void )  
{  
   char buffer[81];  
   int  i, ch;  
  
   // Read in first 80 characters and place them in "buffer":  
   ch = _fgetchar();  
   for( i=0; (i < 80 ) && ( feof( stdin ) == 0 ); i++ )  
   {  
      buffer[i] = (char)ch;  
      ch = _fgetchar();  
   }  
  
   // Add null to end string   
   buffer[i] = '\0';  
   printf( "%s\n", buffer );  
}  
```  
  
  **`Line one. Line two.`Line one.**  
**Line two.**   
## .NET Framework Equivalent  
  
-   [System::IO::StreamReader::Read](https://msdn.microsoft.com/en-us/library/system.io.streamreader.read.aspx)  
  
-   [System::Console::Read](https://msdn.microsoft.com/en-us/library/system.console.read.aspx)  
  
## See Also  
 [Stream I/O](../vs140/Stream-I-O.md)   
 [fputc, fputwc](../vs140/fputc--fputwc.md)   
 [getc, getwc](../vs140/getc--getwc.md)