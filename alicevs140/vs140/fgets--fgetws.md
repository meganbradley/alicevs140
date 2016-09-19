---
title: "fgets, fgetws"
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
  - fgets
  - fgetws
apilocation: 
  - msvcr100.dll
  - msvcr90.dll
  - msvcr80.dll
  - msvcr120.dll
  - msvcr110.dll
  - msvcrt.dll
  - msvcr110_clr0400.dll
apitype: DLLExport
ms.assetid: ad549bb5-df98-4ccd-a53f-95114e60c4fc
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# fgets, fgetws
Get a string from a stream.  
  
## Syntax  
  
```  
char *fgets(   
   char *str,  
   int n,  
   FILE *stream   
);  
wchar_t *fgetws(   
   wchar_t *str,  
   int n,  
   FILE *stream   
);  
```  
  
#### Parameters  
 `str`  
 Storage location for data.  
  
 `n`  
 Maximum number of characters to read.  
  
 `stream`  
 Pointer to `FILE` structure.  
  
## Return Value  
 Each of these functions returns `str`. `NULL` is returned to indicate an error or an end-of-file condition. Use `feof` or `ferror` to determine whether an error occurred. If `str` or `stream` is a null pointer, or `n` is less than or equal to zero, this function invokes the invalid parameter handler, as described in [Parameter Validation](../vs140/Parameter-Validation.md). If execution is allowed to continue, `errno` is set to `EINVAL` and the function returns `NULL`.  
  
 See [_doserrno, errno, _sys_errlist, and _sys_nerr](../vs140/errno--_doserrno--_sys_errlist--and-_sys_nerr.md) for more information on these, and other, error codes.  
  
## Remarks  
 The `fgets` function reads a string from the input `stream` argument and stores it in `str`. `fgets` reads characters from the current stream position to and including the first newline character, to the end of the stream, or until the number of characters read is equal to `n` – 1, whichever comes first. The result stored in `str` is appended with a null character. The newline character, if read, is included in the string.  
  
 `fgetws` is a wide-character version of `fgets`.  
  
 `fgetws` reads the wide-character argument `str` as a multibyte-character string or a wide-character string according to whether `stream` is opened in text mode or binary mode, respectively. For more information about using text and binary modes in Unicode and multibyte stream-I/O, see [Text and Binary Mode File I/O](../vs140/Text-and-Binary-Mode-File-I-O.md) and [Unicode Stream I/O in Text and Binary Modes](../vs140/Unicode-Stream-I-O-in-Text-and-Binary-Modes.md).  
  
### Generic-Text Routine Mappings  
  
|TCHAR.H routine|_UNICODE & _MBCS not defined|_MBCS defined|_UNICODE defined|  
|---------------------|------------------------------------|--------------------|-----------------------|  
|`_fgetts`|`fgets`|`fgets`|`fgetws`|  
  
## Requirements  
  
|Function|Required header|  
|--------------|---------------------|  
|`fgets`|<stdio.h>|  
|`fgetws`|<stdio.h> or <wchar.h>|  
  
 For additional compatibility information, see [Compatibility](../vs140/Compatibility.md) in the Introduction.  
  
## Example  
  
```  
// crt_fgets.c  
// This program uses fgets to display  
// a line from a file on the screen.  
//  
  
#include <stdio.h>  
  
int main( void )  
{  
   FILE *stream;  
   char line[100];  
  
   if( fopen_s( &stream, "crt_fgets.txt", "r" ) == 0 )  
   {  
      if( fgets( line, 100, stream ) == NULL)  
         printf( "fgets error\n" );  
      else  
         printf( "%s", line);  
      fclose( stream );  
   }  
}  
```  
  
## Input: crt_fgets.txt  
  
```  
Line one.  
Line two.  
```  
  
### Output  
  
```  
Line one.  
```  
  
## .NET Framework Equivalent  
  
-   [System::IO::StreamReader::ReadLine](https://msdn.microsoft.com/en-us/library/system.io.streamreader.readline.aspx)  
  
-   [System::IO::TextReader::ReadBlock](https://msdn.microsoft.com/en-us/library/system.io.textreader.readblock.aspx)  
  
## See Also  
 [Stream I/O](../vs140/Stream-I-O.md)   
 [fputs, fputws](../vs140/fputs--fputws.md)   
 [gets, _getws](../vs140/gets--_getws.md)   
 [puts, _putws](../vs140/puts--_putws.md)