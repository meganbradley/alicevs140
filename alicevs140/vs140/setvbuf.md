---
title: "setvbuf"
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
  - setvbuf
apilocation: 
  - msvcr90.dll
  - msvcrt.dll
  - msvcr80.dll
  - msvcr120.dll
  - msvcr110_clr0400.dll
  - msvcr100.dll
  - msvcr110.dll
apitype: DLLExport
ms.assetid: 6aa5aa37-3408-4fa0-992f-87f9f9c4baea
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# setvbuf
Controls stream buffering and buffer size.  
  
## Syntax  
  
```  
int setvbuf(  
   FILE *stream,  
   char *buffer,  
   int mode,  
   size_t size   
);  
```  
  
#### Parameters  
 `stream`  
 Pointer to `FILE` structure.  
  
 `buffer`  
 User-allocated buffer.  
  
 `mode`  
 Mode of buffering.  
  
 `size`  
 Buffer size in bytes. Allowable range: 2 <= `size` <= INT_MAX (2147483647). Internally, the value supplied for `size` is rounded down to the nearest multiple of 2.  
  
## Return Value  
 Returns 0 if successful.  
  
 If `stream` is `NULL`, or if `mode` or `size` is not within a valid change, the invalid parameter handler is invoked, as described in [Parameter Validation](../vs140/Parameter-Validation.md). If execution is allowed to continue, this function returns -1 and sets `errno` to `EINVAL`.  
  
 For information on these and other error codes, see [_doserrno, errno, _sys_errlist, and _sys_nerr](../vs140/errno--_doserrno--_sys_errlist--and-_sys_nerr.md).  
  
## Remarks  
 The `setvbuf` function allows the program to control both buffering and buffer size for `stream`. `stream` must refer to an open file that has not undergone an I/O operation since it was opened. The array pointed to by `buffer` is used as the buffer, unless it is `NULL`, in which case `setvbuf` uses an automatically allocated buffer of length `size`/2 * 2 bytes.  
  
 The mode must be `_IOFBF`, `_IOLBF`, or `_IONBF`. If `mode` is `_IOFBF` or `_IOLBF`, then `size` is used as the size of the buffer. If `mode` is `_IONBF`, the stream is unbuffered and `size` and `buffer` are ignored. Values for `mode` and their meanings are:  
  
 `_IOFBF`  
 Full buffering; that is, `buffer` is used as the buffer and `size` is used as the size of the buffer. If `buffer` is `NULL`, an automatically allocated buffer `size` bytes long is used.  
  
 `_IOLBF`  
 For some systems, this provides line buffering. However, for Win32, the behavior is the same as `_IOFBF` - Full Buffering.  
  
 `_IONBF`  
 No buffer is used, regardless of `buffer` or `size`.  
  
## Requirements  
  
|Routine|Required header|  
|-------------|---------------------|  
|`setvbuf`|<stdio.h>|  
  
 For additional compatibility information, see [Compatibility](../vs140/Compatibility.md) in the Introduction.  
  
## Libraries  
 All versions of the [C run-time libraries](../vs140/CRT-Library-Features.md).  
  
## Example  
  
```  
// crt_setvbuf.c  
// This program opens two streams: stream1  
// and stream2. It then uses setvbuf to give stream1 a  
// user-defined buffer of 1024 bytes and stream2 no buffer.  
//  
  
#include <stdio.h>  
  
int main( void )  
{  
   char buf[1024];  
   FILE *stream1, *stream2;  
  
   if( fopen_s( &stream1, "data1", "a" ) == 0 &&  
       fopen_s( &stream2, "data2", "w" ) == 0 )  
   {  
      if( setvbuf( stream1, buf, _IOFBF, sizeof( buf ) ) != 0 )  
         printf( "Incorrect type or size of buffer for stream1\n" );  
      else  
         printf( "'stream1' now has a buffer of 1024 bytes\n" );  
      if( setvbuf( stream2, NULL, _IONBF, 0 ) != 0 )  
         printf( "Incorrect type or size of buffer for stream2\n" );  
      else  
         printf( "'stream2' now has no buffer\n" );  
      _fcloseall();  
   }  
}  
```  
  
 **'stream1' now has a buffer of 1024 bytes**  
**'stream2' now has no buffer**   
## .NET Framework Equivalent  
 Not applicable. To call the standard C function, use `PInvoke`. For more information, see [Platform Invoke Examples](assetId:///15926806-f0b7-487e-93a6-4e9367ec689f).  
  
## See Also  
 [Stream I/O](../vs140/Stream-I-O.md)   
 [fclose, _fcloseall](../vs140/fclose--_fcloseall.md)   
 [fflush](../vs140/fflush.md)   
 [fopen, _wfopen](../vs140/fopen--_wfopen.md)   
 [setbuf](../vs140/setbuf.md)