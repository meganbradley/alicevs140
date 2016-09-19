---
title: "fgetc, fgetwc"
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
  - fgetwc
  - fgetc
apilocation: 
  - msvcr80.dll
  - msvcr110_clr0400.dll
  - msvcr90.dll
  - msvcr120.dll
  - msvcrt.dll
  - msvcr100.dll
  - msvcr110.dll
apitype: DLLExport
ms.assetid: 13348b7b-dc86-421c-9d6c-611ca79c8338
caps.latest.revision: 20
translation.priority.ht: 
  - de-de
  - ja-jp
---
# fgetc, fgetwc
Read a character from a stream.  
  
## Syntax  
  
```  
int fgetc(   
   FILE *stream   
);  
wint_t fgetwc(   
   FILE *stream   
);  
```  
  
#### Parameters  
 `stream`  
 Pointer to `FILE` structure.  
  
## Return Value  
 `fgetc` returns the character read as an `int` or returns `EOF` to indicate an error or end of file. `fgetwc` returns, as a [wint_t](../vs140/Standard-Types.md), the wide character that corresponds to the character read or returns `WEOF` to indicate an error or end of file. For both functions, use `feof` or `ferror` to distinguish between an error and an end-of-file condition. If a read error occurs, the error indicator for the stream is set. If `stream` is `NULL`, `fgetc` and `fgetwc` invoke the invalid parameter handler, as described in [Parameter Validation](../vs140/Parameter-Validation.md). If execution is allowed to continue, these functions set `errno` to `EINVAL` and return `EOF`.  
  
## Remarks  
 Each of these functions reads a single character from the current position of the file associated with `stream`. The function then increments the associated file pointer (if defined) to point to the next character. If the stream is at end of file, the end-of-file indicator for the stream is set.  
  
 `fgetc` is equivalent to `getc`, but is implemented only as a function, rather than as a function and a macro.  
  
 `fgetwc` is the wide-character version of `fgetc`; it reads `c` as a multibyte character or a wide character according to whether `stream` is opened in text mode or binary mode.  
  
 The versions with the `_nolock` suffix are identical except that they are not protected from interference by other threads.  
  
 For more information about processing wide characters and multibyte characters in text and binary modes, see [Unicode Stream I/O in Text and Binary Modes](../vs140/Unicode-Stream-I-O-in-Text-and-Binary-Modes.md).  
  
### Generic-Text Routine Mappings  
  
|TCHAR.H routine|_UNICODE & _MBCS not defined|_MBCS defined|_UNICODE defined|  
|---------------------|------------------------------------|--------------------|-----------------------|  
|`_fgettc`|`fgetc`|`fgetc`|`fgetwc`|  
  
## Requirements  
  
|Function|Required header|  
|--------------|---------------------|  
|`fgetc`|<stdio.h>|  
|`fgetwc`|<stdio.h> or <wchar.h>|  
  
 For additional compatibility information, see [Compatibility](../vs140/Compatibility.md) in the Introduction.  
  
## Example  
  
```  
// crt_fgetc.c  
// This program uses getc to read the first  
// 80 input characters (or until the end of input)  
// and place them into a string named buffer.  
  
#include <stdio.h>  
#include <stdlib.h>  
  
int main( void )  
{  
   FILE *stream;  
   char buffer[81];  
   int  i, ch;  
  
   // Open file to read line from:  
   fopen_s( &stream, "crt_fgetc.txt", "r" );  
   if( stream == NULL )  
      exit( 0 );  
  
   // Read in first 80 characters and place them in "buffer":   
   ch = fgetc( stream );  
   for( i=0; (i < 80 ) && ( feof( stream ) == 0 ); i++ )  
   {  
      buffer[i] = (char)ch;  
      ch = fgetc( stream );  
   }  
  
   // Add null to end string   
   buffer[i] = '\0';  
   printf( "%s\n", buffer );  
   fclose( stream );  
}  
```  
  
## Input: crt_fgetc.txt  
  
```  
Line one.  
Line two.  
```  
  
### Output  
  
```  
Line one.  
Line two.  
```  
  
## .NET Framework Equivalent  
  
-   [System::IO::StreamReader::Read](https://msdn.microsoft.com/en-us/library/system.io.streamreader.read.aspx)  
  
-   [System::Console::Read](https://msdn.microsoft.com/en-us/library/system.console.read.aspx)  
  
## See Also  
 [Stream I/O](../vs140/Stream-I-O.md)   
 [fputc, fputwc](../vs140/fputc--fputwc.md)   
 [getc, getwc](../vs140/getc--getwc.md)