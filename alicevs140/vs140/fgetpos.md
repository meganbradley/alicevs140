---
title: "fgetpos"
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
  - fgetpos
apilocation: 
  - msvcr120.dll
  - msvcr90.dll
  - msvcr110.dll
  - msvcr100.dll
  - msvcr80.dll
  - msvcr110_clr0400.dll
  - msvcrt.dll
apitype: DLLExport
ms.assetid: bfa05c38-1135-418c-bda1-d41be51acb62
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# fgetpos
Gets a stream's file-position indicator.  
  
## Syntax  
  
```  
int fgetpos(   
   FILE *stream,  
   fpos_t *pos   
);  
```  
  
#### Parameters  
 `stream`  
 Target stream.  
  
 `pos`  
 Position-indicator storage.  
  
## Return Value  
 If successful, `fgetpos` returns 0. On failure, it returns a nonzero value and sets `errno` to one of the following manifest constants (defined in STDIO.H): `EBADF`, which means the specified stream is not a valid file pointer or is not accessible, or `EINVAL`, which means the `stream` value or the value of `pos` is invalid, such as if either is a null pointer. If `stream` or `pos` is a `NULL` pointer, the function invokes the invalid parameter handler, as described in [Parameter Validation](../vs140/Parameter-Validation.md).  
  
## Remarks  
 The `fgetpos` function gets the current value of the `stream` argument's file-position indicator and stores it in the object pointed to by `pos`. The `fsetpos` function can later use information stored in `pos` to reset the `stream` argument's pointer to its position at the time `fgetpos` was called. The `pos` value is stored in an internal format and is intended for use only by `fgetpos` and `fsetpos`.  
  
## Requirements  
  
|Function|Required header|  
|--------------|---------------------|  
|`fgetpos`|<stdio.h>|  
  
 For additional compatibility information, see [Compatibility](../vs140/Compatibility.md) in the Introduction.  
  
## Example  
  
```  
// crt_fgetpos.c  
// This program uses fgetpos and fsetpos to  
// return to a location in a file.  
  
#include <stdio.h>  
  
int main( void )  
{  
   FILE   *stream;  
   fpos_t pos;  
   char   buffer[20];  
  
   if( fopen_s( &stream, "crt_fgetpos.txt", "rb" ) ) {  
      perror( "Trouble opening file" );  
      return -1;  
   }  
  
   // Read some data and then save the position.   
   fread( buffer, sizeof( char ), 8, stream );  
   if( fgetpos( stream, &pos ) != 0 ) {  
      perror( "fgetpos error" );  
      return -1;  
   }  
  
   fread( buffer, sizeof( char ), 13, stream );  
   printf( "after fgetpos: %.13s\n", buffer );  
  
   // Restore to old position and read data   
   if( fsetpos( stream, &pos ) != 0 ) {  
      perror( "fsetpos error" );  
      return -1;  
   }  
  
   fread( buffer, sizeof( char ), 13, stream );  
   printf( "after fsetpos: %.13s\n", buffer );  
   fclose( stream );  
}  
```  
  
## Input: crt_fgetpos.txt  
  
```  
fgetpos gets a stream's file-position indicator.  
```  
  
### Output crt_fgetpos.txt  
  
```  
after fgetpos: gets a stream  
after fsetpos: gets a stream  
```  
  
## .NET Framework Equivalent  
 [System::IO::FileStream::Position](https://msdn.microsoft.com/en-us/library/system.io.filestream.position.aspx)  
  
## See Also  
 [Stream I/O](../vs140/Stream-I-O.md)   
 [fsetpos](../vs140/fsetpos.md)