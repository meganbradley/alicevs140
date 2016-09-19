---
title: "fseek, _fseeki64"
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
  - _fseeki64
  - fseek
apilocation: 
  - msvcr120.dll
  - msvcr110.dll
  - msvcr80.dll
  - msvcr90.dll
  - msvcr100.dll
  - msvcrt.dll
  - msvcr110_clr0400.dll
apitype: DLLExport
ms.assetid: f6bb1f8b-891c-426e-9e14-0e7e5c62df70
caps.latest.revision: 23
translation.priority.ht: 
  - de-de
  - ja-jp
---
# fseek, _fseeki64
Moves the file pointer to a specified location.  
  
## Syntax  
  
```  
int fseek(   
   FILE *stream,  
   long offset,  
   int origin   
);  
int _fseeki64(   
   FILE *stream,  
   __int64 offset,  
   int origin   
);  
```  
  
#### Parameters  
 `stream`  
 Pointer to `FILE` structure.  
  
 `offset`  
 Number of bytes from `origin`.  
  
 `origin`  
 Initial position.  
  
## Return Value  
 If successful, `fseek` and `_fseeki64` returns 0. Otherwise, it returns a nonzero value. On devices incapable of seeking, the return value is undefined. If `stream` is a null pointer, or if `origin` is not one of allowed values described below, `fseek` and `_fseeki64` invoke the invalid parameter handler, as described in [Parameter Validation](../vs140/Parameter-Validation.md). If execution is allowed to continue, these functions set `errno` to `EINVAL` and return -1.  
  
## Remarks  
 The `fseek` and `_fseeki64` functions moves the file pointer (if any) associated with `stream` to a new location that is `offset` bytes from `origin`*.* The next operation on the stream takes place at the new location. On a stream open for update, the next operation can be either a read or a write. The argument origin must be one of the following constants, defined in STDIO.H:  
  
 `SEEK_CUR`  
 Current position of file pointer.  
  
 `SEEK_END`  
 End of file.  
  
 `SEEK_SET`  
 Beginning of file.  
  
 You can use `fseek` and `_fseeki64` to reposition the pointer anywhere in a file. The pointer can also be positioned beyond the end of the file. `fseek` and `_fseeki64`clears the end-of-file indicator and negates the effect of any prior `ungetc` calls against `stream`.  
  
 When a file is opened for appending data, the current file position is determined by the last I/O operation, not by where the next write would occur. If no I/O operation has yet occurred on a file opened for appending, the file position is the start of the file.  
  
 For streams opened in text mode, `fseek` and `_fseeki64`have limited use, because carriage return–linefeed translations can cause `fseek` and `_fseeki64`to produce unexpected results. The only `fseek` and `_fseeki64`operations guaranteed to work on streams opened in text mode are:  
  
-   Seeking with an offset of 0 relative to any of the origin values.  
  
-   Seeking from the beginning of the file with an offset value returned from a call to `ftell` when using `fseek`or `_ftelli64`when using`_fseeki64`.  
  
 Also in text mode, CTRL+Z is interpreted as an end-of-file character on input. In files opened for reading/writing, `fopen` and all related routines check for a CTRL+Z at the end of the file and remove it if possible. This is done because using the combination of `fseek` and `ftell`or`_fseeki64` and `_ftelli64`, to move within a file that ends with a CTRL+Z may cause `fseek` or `_fseeki64` to behave improperly near the end of the file.  
  
 When the CRT opens a file that begins with a Byte Order Mark (BOM), the file pointer is positioned after the BOM (that is, at the start of the file's actual content). If you have to `fseek` to the beginning of the file, use `ftell` to get the initial position and `fseek` to it rather than to position 0.  
  
 This function locks out other threads during execution and is therefore thread-safe. For a non-locking version, see [_fseek_nolock](../vs140/_fseek_nolock--_fseeki64_nolock.md).  
  
## Requirements  
  
|Function|Required header|  
|--------------|---------------------|  
|`fseek`|<stdio.h>|  
|`_fseeki64`|<stdio.h>|  
  
 For additional compatibility information, see [Compatibility](../vs140/Compatibility.md) in the Introduction.  
  
## Example  
  
```  
// crt_fseek.c  
// This program opens the file FSEEK.OUT and  
// moves the pointer to the file's beginning.  
  
#include <stdio.h>  
  
int main( void )  
{  
   FILE *stream;  
   char line[81];  
   int  result;  
  
   if ( fopen_s( &stream, "fseek.out", "w+" ) != 0 )  
   {  
      printf( "The file fseek.out was not opened\n" );  
      return -1;  
   }  
   fprintf( stream, "The fseek begins here: "  
                    "This is the file 'fseek.out'.\n" );  
   result = fseek( stream, 23L, SEEK_SET);  
   if( result )  
      perror( "Fseek failed" );  
   else  
   {  
      printf( "File pointer is set to middle of first line.\n" );  
      fgets( line, 80, stream );  
      printf( "%s", line );  
    }  
   fclose( stream );  
}  
```  
  
 **File pointer is set to middle of first line.**  
**This is the file 'fseek.out'.**   
## .NET Framework Equivalent  
  
-   [System::IO::FileStream::Position](https://msdn.microsoft.com/en-us/library/system.io.filestream.position.aspx)  
  
-   [System::IO::FileStream::Seek](https://msdn.microsoft.com/en-us/library/system.io.filestream.seek.aspx)  
  
## See Also  
 [Stream I/O](../vs140/Stream-I-O.md)   
 [fopen, _wfopen](../vs140/fopen--_wfopen.md)   
 [ftell](../vs140/ftell--_ftelli64.md)   
 [_lseek, _lseeki64](../vs140/_lseek--_lseeki64.md)   
 [rewind](../vs140/rewind.md)