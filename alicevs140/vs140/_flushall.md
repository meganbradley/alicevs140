---
title: "_flushall"
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
  - _flushall
apilocation: 
  - msvcr100.dll
  - msvcr80.dll
  - msvcr110.dll
  - msvcr120.dll
  - msvcrt.dll
  - msvcr110_clr0400.dll
  - msvcr90.dll
apitype: DLLExport
ms.assetid: 2cd73562-6d00-4ca2-b13c-80d0ae7870b5
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _flushall
Flushes all streams; clears all buffers.  
  
## Syntax  
  
```  
int _flushall( void );  
```  
  
## Return Value  
 `_flushall` returns the number of open streams (input and output). There is no error return.  
  
## Remarks  
 By default, the `_flushall` function writes to appropriate files the contents of all buffers associated with open output streams. All buffers associated with open input streams are cleared of their current contents. (These buffers are normally maintained by the operating system, which determines the optimal time to write the data automatically to disk: when a buffer is full, when a stream is closed, or when a program terminates normally without closing streams.)  
  
 If a read follows a call to `_flushall`, new data is read from the input files into the buffers. All streams remain open after the call to `_flushall`.  
  
 The commit-to-disk feature of the run-time library lets you ensure that critical data is written directly to disk rather than to the operating system buffers. Without rewriting an existing program, you can enable this feature by linking the program's object files with Commode.obj. In the resulting executable file, calls to `_flushall` write the contents of all buffers to disk. Only `_flushall` and `fflush` are affected by Commode.obj.  
  
 For information about controlling the commit-to-disk feature, see [Stream I/O](../vs140/Stream-I-O.md), [fopen](../vs140/fopen--_wfopen.md), and [_fdopen](../vs140/_fdopen--_wfdopen.md).  
  
## Requirements  
  
|Function|Required header|  
|--------------|---------------------|  
|`_flushall`|<stdio.h>|  
  
 For more compatibility information, see [Compatibility](../vs140/Compatibility.md) in the Introduction.  
  
## Example  
  
```  
// crt_flushall.c  
// This program uses _flushall  
// to flush all open buffers.  
  
#include <stdio.h>  
  
int main( void )  
{  
   int numflushed;  
  
   numflushed = _flushall();  
   printf( "There were %d streams flushed\n", numflushed );  
}  
```  
  
 **There were 3 streams flushed**   
## .NET Framework Equivalent  
  
-   [System::IO::FileStream::Flush](https://msdn.microsoft.com/en-us/library/2bw4h516.aspx)  
  
-   [System::IO::StreamWriter::Flush](https://msdn.microsoft.com/en-us/library/system.io.streamwriter.flush.aspx)  
  
-   [System::IO::TextWriter::Flush](https://msdn.microsoft.com/en-us/library/system.io.textwriter.flush.aspx)  
  
-   [System::IO::BinaryWriter::Flush](https://msdn.microsoft.com/en-us/library/system.io.binarywriter.flush.aspx)  
  
## See Also  
 [Stream I/O](../vs140/Stream-I-O.md)   
 [_commit](../vs140/_commit.md)   
 [fclose, _fcloseall](../vs140/fclose--_fcloseall.md)   
 [fflush](../vs140/fflush.md)   
 [setvbuf](../vs140/setvbuf.md)