---
title: "rewind"
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
  - rewind
apilocation: 
  - msvcr90.dll
  - msvcr120.dll
  - msvcr80.dll
  - msvcrt.dll
  - msvcr100.dll
  - msvcr110.dll
  - msvcr110_clr0400.dll
apitype: DLLExport
ms.assetid: 1a460ce1-28d8-4b5e-83a6-633dca29c28a
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# rewind
Repositions the file pointer to the beginning of a file.  
  
## Syntax  
  
```  
  
      void rewind(  
   FILE *stream   
);  
```  
  
#### Parameters  
 `stream`  
 Pointer to **FILE** structure.  
  
## Remarks  
 The **rewind** function repositions the file pointer associated with `stream` to the beginning of the file. A call to **rewind** is similar to  
  
 **(void) fseek(** `stream`**, 0L,** `SEEK_SET` **);**  
  
 However, unlike `fseek`, **rewind** clears the error indicators for the stream as well as the end-of-file indicator. Also, unlike `fseek`, **rewind** does not return a value to indicate whether the pointer was successfully moved.  
  
 To clear the keyboard buffer, use **rewind** with the stream `stdin`, which is associated with the keyboard by default.  
  
 If stream is a `NULL` pointer, the invalid parameter handler is invoked, as described in [Parameter Validation](../vs140/Parameter-Validation.md). If execution is allowed to continue, this function returns and `errno` is set to `EINVAL`.  
  
 For information on these and other error codes, see [_doserrno, errno, _sys_errlist, and _sys_nerr](../vs140/errno--_doserrno--_sys_errlist--and-_sys_nerr.md).  
  
## Requirements  
  
|Routine|Required header|  
|-------------|---------------------|  
|**rewind**|<stdio.h>|  
  
 For additional compatibility information, see [Compatibility](../vs140/Compatibility.md) in the Introduction.  
  
## Libraries  
 All versions of the [C run-time libraries](../vs140/CRT-Library-Features.md).  
  
## Example  
  
```  
// crt_rewind.c  
/* This program first opens a file named  
 * crt_rewind.out for input and output and writes two  
 * integers to the file. Next, it uses rewind to  
 * reposition the file pointer to the beginning of  
 * the file and reads the data back in.  
 */  
#include <stdio.h>  
  
int main( void )  
{  
   FILE *stream;  
   int data1, data2;  
  
   data1 = 1;  
   data2 = -37;  
  
   fopen_s( &stream, "crt_rewind.out", "w+" );  
   if( stream != NULL )  
   {  
      fprintf( stream, "%d %d", data1, data2 );  
      printf( "The values written are: %d and %d\n", data1, data2 );  
      rewind( stream );  
      fscanf_s( stream, "%d %d", &data1, &data2 );  
      printf( "The values read are: %d and %d\n", data1, data2 );  
      fclose( stream );  
   }  
}  
```  
  
## Output  
  
```  
The values written are: 1 and -37  
The values read are: 1 and -37  
```  
  
## .NET Framework Equivalent  
 Not applicable. To call the standard C function, use `PInvoke`. For more information, see [Platform Invoke Examples](assetId:///15926806-f0b7-487e-93a6-4e9367ec689f).  
  
## See Also  
 [Stream I/O](../vs140/Stream-I-O.md)