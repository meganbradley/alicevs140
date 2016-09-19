---
title: "_tell, _telli64"
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
  - _telli64
  - _tell
apilocation: 
  - msvcr100.dll
  - msvcr110.dll
  - msvcr120.dll
  - msvcr90.dll
  - msvcr80.dll
  - msvcrt.dll
  - msvcr110_clr0400.dll
apitype: DLLExport
ms.assetid: 1500e8f9-8fec-4253-9eec-ec66125dfc9b
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _tell, _telli64
Get the position of the file pointer.  
  
## Syntax  
  
```  
long _tell(  
   int handle  
);  
__int64 _telli64(  
   int handle   
);  
```  
  
#### Parameters  
 `handle`  
 File descriptor referring to open file.  
  
## Return Value  
 The current position of the file pointer. On devices incapable of seeking, the return value is undefined.  
  
 A return value of –1L indicates an error. If `handle` is an invalid file descriptor, the invalid parameter handler is invoked, as described in [Parameter Validation](../vs140/Parameter-Validation.md). If execution is allowed to continue, these functions set `errno` to `EBADF` and return -1L.  
  
 See [_doserrno, errno, _sys_errlist, and _sys_nerr](../vs140/errno--_doserrno--_sys_errlist--and-_sys_nerr.md) for more information on this, and other, return codes.  
  
## Remarks  
 The `_tell` function gets the current position of the file pointer (if any) associated with the `handle` argument. The position is expressed as the number of bytes from the beginning of the file. For the `_telli64` function, this value is expressed as a 64-bit integer.  
  
## Requirements  
  
|Routine|Required header|  
|-------------|---------------------|  
|`_tell`, `_telli64`|<io.h>|  
  
 For additional compatibility information, see [Compatibility](../vs140/Compatibility.md) in the Introduction.  
  
## Example  
  
```  
// crt_tell.c  
// This program uses _tell to tell the  
// file pointer position after a file read.  
//  
  
#include <io.h>  
#include <stdio.h>  
#include <fcntl.h>  
#include <share.h>  
#include <string.h>  
  
int main( void )  
{  
   int  fh;  
   char buffer[500];  
  
   if ( _sopen_s( &fh, "crt_tell.txt", _O_RDONLY, _SH_DENYNO, 0) )  
   {  
      char buff[50];  
      _strerror_s( buff, sizeof(buff), NULL );  
      printf( buff );  
      exit( -1 );  
   }  
  
   if( _read( fh, buffer, 500 ) > 0 )  
      printf( "Current file position is: %d\n", _tell( fh ) );  
   _close( fh );  
}  
```  
  
## Input: crt_tell.txt  
  
```  
Line one.  
Line two.  
```  
  
### Output  
  
```  
Current file position is: 20  
```  
  
## See Also  
 [Low-Level I/O](../vs140/Low-Level-I-O.md)   
 [ftell, _ftelli64](../vs140/ftell--_ftelli64.md)   
 [_lseek, _lseeki64](../vs140/_lseek--_lseeki64.md)