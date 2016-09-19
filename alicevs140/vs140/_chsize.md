---
title: "_chsize"
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
  - _chsize
apilocation: 
  - msvcr90.dll
  - msvcr120.dll
  - msvcr110_clr0400.dll
  - msvcr80.dll
  - msvcrt.dll
  - msvcr100.dll
  - msvcr110.dll
apitype: DLLExport
ms.assetid: b3e881c5-7b27-4837-a3d4-c51591ab10ff
caps.latest.revision: 21
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _chsize
Changes the size of a file. A more secure version is available; see [_chsize_s](../vs140/_chsize_s.md).  
  
## Syntax  
  
```  
int _chsize(   
   int fd,  
   long size   
);  
```  
  
#### Parameters  
 `fd`  
 File descriptor referring to an open file.  
  
 `size`  
 New length of the file in bytes.  
  
## Return Value  
 `_chsize` returns the value 0 if the file size is successfully changed. A return value of –1 indicates an error: `errno` is set to `EACCES` if the specified file is locked against access, to `EBADF` if the specified file is read-only or the descriptor is invalid, `ENOSPC` if no space is left on the device, or `EINVAL` if `size` is less than zero.  
  
 See [_doserrno, errno, _sys_errlist, and _sys_nerr](../vs140/errno--_doserrno--_sys_errlist--and-_sys_nerr.md) for more information on these, and other, return codes.  
  
## Remarks  
 The `_chsize` function extends or truncates the file associated with `fd` to the length specified by `size`. The file must be open in a mode that permits writing. Null characters ('\0') are appended if the file is extended. If the file is truncated, all data from the end of the shortened file to the original length of the file is lost.  
  
 This function validates its parameters. If `size` is less than zero or `fd` is a bad file descriptor, the invalid parameter handler is invoked, as described in [Parameter Validation](../vs140/Parameter-Validation.md).  
  
## Requirements  
  
|Routine|Required header|Optional header|  
|-------------|---------------------|---------------------|  
|`_chsize`|<io.h>|<errno.h>|  
  
 For more compatibility information, see [Compatibility](../vs140/Compatibility.md) in the Introduction.  
  
## Example  
  
```  
// crt_chsize.c  
// This program uses _filelength to report the size  
// of a file before and after modifying it with _chsize.  
  
#include <io.h>  
#include <fcntl.h>  
#include <sys/types.h>  
#include <sys/stat.h>  
#include <stdio.h>  
#include <share.h>  
  
int main( void )  
{  
   int fh, result;  
   unsigned int nbytes = BUFSIZ;  
  
   // Open a file   
   if( _sopen_s( &fh, "data", _O_RDWR | _O_CREAT, _SH_DENYNO,  
                 _S_IREAD | _S_IWRITE ) == 0 )  
   {  
      printf( "File length before: %ld\n", _filelength( fh ) );  
      if( ( result = _chsize( fh, 329678 ) ) == 0 )  
         printf( "Size successfully changed\n" );  
      else  
         printf( "Problem in changing the size\n" );  
      printf( "File length after:  %ld\n", _filelength( fh ) );  
      _close( fh );  
   }  
}  
```  
  
 **File length before: 0**  
**Size successfully changed**  
**File length after:  329678**   
## .NET Framework Equivalent  
  
-   [System::IO::Stream::SetLength](https://msdn.microsoft.com/en-us/library/system.io.stream.setlength.aspx)  
  
-   [System::IO::FileStream::SetLength](https://msdn.microsoft.com/en-us/library/system.io.filestream.setlength.aspx)  
  
## See Also  
 [File Handling](../Topic/File%20Handling.md)   
 [_close](../vs140/_close.md)   
 [_sopen, _wsopen](../vs140/_sopen--_wsopen.md)   
 [_open, _wopen](../Topic/_open,%20_wopen.md)