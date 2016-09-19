---
title: "_getw"
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
  - _getw
apilocation: 
  - msvcrt.dll
  - msvcr90.dll
  - msvcr100.dll
  - msvcr110.dll
  - msvcr120.dll
  - msvcr110_clr0400.dll
  - msvcr80.dll
apitype: DLLExport
ms.assetid: ef75facc-b84e-470f-9f5f-8746c90822a0
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _getw
Gets an integer from a stream.  
  
## Syntax  
  
```  
int _getw(   
   FILE *stream   
);  
```  
  
#### Parameters  
 `stream`  
 Pointer to the `FILE` structure.  
  
## Return Value  
 `_getw` returns the integer value read. A return value of `EOF` indicates either an error or end of file. However, because the `EOF` value is also a legitimate integer value, use `feof` or `ferror` to verify an end-of-file or error condition. If `stream` is `NULL`, the invalid parameter handler is invoked, as described in [Parameter Validation](../vs140/Parameter-Validation.md). If execution is allowed to continue, `errno` is set to `EINVAL` and the function returns `EOF`.  
  
## Remarks  
 The `_getw` function reads the next binary value of type `int` from the file associated with `stream` and increments the associated file pointer (if there is one) to point to the next unread character. `_getw` does not assume any special alignment of items in the stream. Problems with porting can occur with `_getw` because the size of the `int` type and the ordering of bytes within the `int` type differ across systems.  
  
## Requirements  
  
|Routine|Required header|  
|-------------|---------------------|  
|`_getw`|<stdio.h>|  
  
 For more compatibility information, see [Compatibility](../vs140/Compatibility.md) in the Introduction.  
  
## Example  
  
```  
// crt_getw.c  
// This program uses _getw to read a word  
// from a stream, then performs an error check.  
  
#include <stdio.h>  
#include <stdlib.h>  
  
int main( void )  
{  
   FILE *stream;  
   int i;  
  
   if( fopen_s( &stream, "crt_getw.txt", "rb" ) )  
      printf( "Couldn't open file\n" );  
   else  
   {  
      // Read a word from the stream:  
      i = _getw( stream );  
  
      // If there is an error...  
      if( ferror( stream ) )  
      {  
         printf( "_getw failed\n" );  
         clearerr_s( stream );  
      }  
      else  
         printf( "First data word in file: 0x%.4x\n", i );  
      fclose( stream );  
   }  
}  
```  
  
## Input: crt_getw.txt  
  
```  
Line one.  
Line two.  
```  
  
### Output  
  
```  
First data word in file: 0x656e694c  
```  
  
## .NET Framework Equivalent  
 Not applicable. To call the standard C function, use `PInvoke`. For more information, see [Platform Invoke Examples](assetId:///15926806-f0b7-487e-93a6-4e9367ec689f).  
  
## See Also  
 [Stream I/O](../vs140/Stream-I-O.md)   
 [_putw](../vs140/_putw.md)