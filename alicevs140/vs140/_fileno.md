---
title: "_fileno"
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
  - _fileno
apilocation: 
  - msvcrt.dll
  - msvcr120.dll
  - msvcr90.dll
  - msvcr100.dll
  - msvcr110_clr0400.dll
  - msvcr110.dll
  - msvcr80.dll
apitype: DLLExport
ms.assetid: 86474174-2f17-4100-bcc4-352dd976c7b5
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _fileno
Gets the file descriptor associated with a stream.  
  
## Syntax  
  
```  
int _fileno(   
   FILE *stream   
);  
```  
  
#### Parameters  
 `stream`  
 Pointer to the `FILE` structure.  
  
## Return Value  
 `_fileno` returns the file descriptor. There is no error return. The result is undefined if `stream` does not specify an open file. If stream is `NULL`, _`fileno` invokes the invalid parameter handler, as described in [Parameter Validation](../vs140/Parameter-Validation.md). If execution is allowed to continue, this function returns -1 and sets `errno` to `EINVAL`.  
  
 For more information about these and other error codes, see [_doserrno, errno, _sys_errlist, and _sys_nerr](../vs140/errno--_doserrno--_sys_errlist--and-_sys_nerr.md).  
  
> [!NOTE]
>  If `stdout` or `stderr` is not associated with an output stream (for example, in a Windows application without a console window), the file descriptor returned is -2. In previous versions, the file descriptor returned was -1. This change allows applications to distinguish this condition from an error.  
  
## Remarks  
 The `_fileno` routine returns the file descriptor currently associated with `stream`. This routine is implemented both as a function and as a macro. For information about choosing either implementation, see [Choosing Between Functions and Macros](../vs140/Recommendations-for-Choosing-Between-Functions-and-Macros.md).  
  
## Requirements  
  
|Function|Required header|  
|--------------|---------------------|  
|`_fileno`|<stdio.h>|  
  
 For more compatibility information, see [Compatibility](../vs140/Compatibility.md) in the Introduction.  
  
## Example  
  
```  
// crt_fileno.c  
// This program uses _fileno to obtain  
// the file descriptor for some standard C streams.  
//  
  
#include <stdio.h>  
  
int main( void )  
{  
   printf( "The file descriptor for stdin is %d\n", _fileno( stdin ) );  
   printf( "The file descriptor for stdout is %d\n", _fileno( stdout ) );  
   printf( "The file descriptor for stderr is %d\n", _fileno( stderr ) );  
}  
```  
  
 **The file descriptor for stdin is 0**  
**The file descriptor for stdout is 1**  
**The file descriptor for stderr is 2**   
## .NET Framework Equivalent  
 [System::IO::FileStream::Handle](https://msdn.microsoft.com/en-us/library/system.io.filestream.handle.aspx)  
  
## See Also  
 [Stream I/O](../vs140/Stream-I-O.md)   
 [_fdopen, _wfdopen](../vs140/_fdopen--_wfdopen.md)   
 [_filelength, _filelengthi64](../vs140/_filelength--_filelengthi64.md)   
 [fopen, _wfopen](../vs140/fopen--_wfopen.md)   
 [freopen, _wfreopen](../Topic/freopen,%20_wfreopen.md)