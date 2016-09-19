---
title: "_filelength, _filelengthi64"
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
  - _filelengthi64
  - _filelength
apilocation: 
  - msvcr100.dll
  - msvcr110.dll
  - msvcrt.dll
  - msvcr90.dll
  - msvcr80.dll
  - msvcr120.dll
  - msvcr110_clr0400.dll
apitype: DLLExport
ms.assetid: 3ab83d5a-543c-4079-b9d9-0abfc7da0275
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _filelength, _filelengthi64
Gets the length of a file.  
  
## Syntax  
  
```  
long _filelength(   
   int fd   
);  
__int64 _filelengthi64(   
   int fd   
);  
```  
  
#### Parameters  
 `fd`  
 Target the file descriptor.  
  
## Return Value  
 Both `_filelength` and `_filelengthi64` return the file length, in bytes, of the target file associated with `fd`. If `fd` is an invalid file descriptor, this function invokes the invalid parameter handler, as described in [Parameter Validation](../vs140/Parameter-Validation.md). If execution is allowed to continue, both functions return –1L to indicate an error and set `errno` to `EBADF`.  
  
## Requirements  
  
|Function|Required header|  
|--------------|---------------------|  
|`_filelength`|<io.h>|  
|`_filelengthi64`|<io.h>|  
  
 For more compatibility information, see [Compatibility](../vs140/Compatibility.md) in the Introduction.  
  
## Example  
 See the example for [_chsize](../vs140/_chsize.md).  
  
## .NET Framework Equivalent  
  
-   [System::IO::Stream::SetLength](https://msdn.microsoft.com/en-us/library/system.io.stream.setlength.aspx)  
  
-   [System::IO::FileStream::SetLength](https://msdn.microsoft.com/en-us/library/system.io.filestream.setlength.aspx)  
  
## See Also  
 [File Handling](../Topic/File%20Handling.md)   
 [_chsize](../vs140/_chsize.md)   
 [_fileno](../vs140/_fileno.md)   
 [_fstat, _fstat32, _fstat64, _fstati64, _fstat32i64, _fstat64i32](../vs140/_fstat--_fstat32--_fstat64--_fstati64--_fstat32i64--_fstat64i32.md)   
 [_fstat, _fstat32, _fstat64, _fstati64, _fstat32i64, _fstat64i32](../vs140/_fstat--_fstat32--_fstat64--_fstati64--_fstat32i64--_fstat64i32.md)   
 [_stat, _wstat Functions](../vs140/_stat--_stat32--_stat64--_stati64--_stat32i64--_stat64i32--_wstat--_wstat32--_wstat64--_wstati64--_wstat32i64--_wstat64i32.md)   
 [_stat, _wstat Functions](../vs140/_stat--_stat32--_stat64--_stati64--_stat32i64--_stat64i32--_wstat--_wstat32--_wstat64--_wstati64--_wstat32i64--_wstat64i32.md)