---
title: "_dup, _dup2"
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
  - _dup
  - _dup2
apilocation: 
  - msvcr120.dll
  - msvcr100.dll
  - msvcr110.dll
  - msvcrt.dll
  - msvcr90.dll
  - msvcr80.dll
  - msvcr110_clr0400.dll
apitype: DLLExport
ms.assetid: 4d07e92c-0d76-4832-a770-dfec0e7a0cfa
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _dup, _dup2
Creates a second file descriptor for an open file (`_dup`), or reassigns a file descriptor (`_dup2`).  
  
## Syntax  
  
```  
int _dup(   
   int fd   
);  
int _dup2(   
   int fd1,  
   int fd2   
);  
```  
  
#### Parameters  
 `fd`, `fd1`  
 File descriptors referring to open file.  
  
 `fd2`  
 Any file descriptor.  
  
## Return Value  
 `_dup` returns a new file descriptor. `_dup2` returns 0 to indicate success. If an error occurs, each function returns –1 and sets `errno` to `EBADF` if the file descriptor is invalid or to `EMFILE` if no more file descriptors are available. In the case of an invalid file descriptor, the function also invokes the invalid parameter handler, as described in [Parameter Validation](../vs140/Parameter-Validation.md).  
  
 For more information about these and other return codes, see [_doserrno, errno, _sys_errlist, and _sys_nerr](../vs140/errno--_doserrno--_sys_errlist--and-_sys_nerr.md).  
  
## Remarks  
 The `_dup` and `_dup2` functions associate a second file descriptor with a currently open file. These functions can be used to associate a predefined file descriptor, such as that for `stdout`, with a different file. Operations on the file can be carried out using either file descriptor. The type of access allowed for the file is unaffected by the creation of a new descriptor. `_dup` returns the next available file descriptor for the given file. `_dup2` forces `fd2` to refer to the same file as `fd1`. If `fd2` is associated with an open file at the time of the call, that file is closed.  
  
 Both `_dup` and `_dup2` accept file descriptors as parameters. To pass a stream `(FILE *)` to either of these functions, use [_fileno](../vs140/_fileno.md). The `fileno` routine returns the file descriptor currently associated with the given stream. The following example shows how to associate `stderr` (defined as `FILE` `*` in Stdio.h) with a file descriptor:  
  
```  
int cstderr = _dup( _fileno( stderr ));  
```  
  
## Requirements  
  
|Routine|Required header|  
|-------------|---------------------|  
|`_dup`|<io.h>|  
|`_dup2`|<io.h>|  
  
 The console is not supported in [!INCLUDE[win8_appname_long](../vs140/includes/win8_appname_long_md.md)] apps. The standard stream handles that are associated with the console—`stdin`, `stdout`, and `stderr`—must be redirected before C run-time functions can use them in [!INCLUDE[win8_appname_long](../vs140/includes/win8_appname_long_md.md)] apps. For more compatibility information, see [Compatibility](../vs140/Compatibility.md).  
  
## Example  
  
```  
// crt_dup.c  
// This program uses the variable old to save  
// the original stdout. It then opens a new file named  
// DataFile and forces stdout to refer to it. Finally, it  
// restores stdout to its original state.  
//  
  
#include <io.h>  
#include <stdlib.h>  
#include <stdio.h>  
  
int main( void )  
{  
   int old;  
   FILE *DataFile;  
  
   old = _dup( 1 );   // "old" now refers to "stdout"   
                      // Note:  file descriptor 1 == "stdout"   
   if( old == -1 )  
   {  
      perror( "_dup( 1 ) failure" );  
      exit( 1 );  
   }  
   _write( old, "This goes to stdout first\n", 26 );  
   if( fopen_s( &DataFile, "data", "w" ) != 0 )  
   {  
      puts( "Can't open file 'data'\n" );  
      exit( 1 );  
   }  
  
   // stdout now refers to file "data"   
   if( -1 == _dup2( _fileno( DataFile ), 1 ) )  
   {  
      perror( "Can't _dup2 stdout" );  
      exit( 1 );  
   }  
   puts( "This goes to file 'data'\n" );  
  
   // Flush stdout stream buffer so it goes to correct file   
   fflush( stdout );  
   fclose( DataFile );  
  
   // Restore original stdout   
   _dup2( old, 1 );  
   puts( "This goes to stdout\n" );  
   puts( "The file 'data' contains:" );  
   _flushall();  
   system( "type data" );  
}  
```  
  
 **This goes to stdout first**  
**This goes to stdout**  
**The file 'data' contains:**  
**This goes to file 'data'**   
## See Also  
 [Low-Level I/O](../vs140/Low-Level-I-O.md)   
 [_close](../vs140/_close.md)   
 [_creat, _wcreat](../vs140/_creat--_wcreat.md)   
 [_open, _wopen](../Topic/_open,%20_wopen.md)