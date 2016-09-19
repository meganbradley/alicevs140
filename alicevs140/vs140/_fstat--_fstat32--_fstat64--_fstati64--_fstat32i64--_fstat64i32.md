---
title: "_fstat, _fstat32, _fstat64, _fstati64, _fstat32i64, _fstat64i32"
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
  - _fstat32
  - _fstat64
  - _fstati64
  - _fstat
  - _fstat64i32
  - _fstat32i64
apilocation: 
  - msvcr80.dll
  - msvcr120.dll
  - msvcr110.dll
  - msvcrt.dll
  - msvcr90.dll
  - msvcr100.dll
  - msvcr110_clr0400.dll
apitype: DLLExport
ms.assetid: 088f5e7a-9636-4cf7-ab8e-e28d2aa4280a
caps.latest.revision: 23
translation.priority.mt: 
  - de-de
  - ja-jp
---
# _fstat, _fstat32, _fstat64, _fstati64, _fstat32i64, _fstat64i32
Gets information about an open file.  
  
## Syntax  
  
```  
int _fstat(   
   int fd,  
   struct _stat *buffer   
);  
int _fstat32(   
   int fd,  
   struct __stat32 *buffer   
);  
int _fstat64(   
   int fd,  
   struct __stat64 *buffer   
);  
int _fstati64(   
   int fd,  
   struct _stati64 *buffer   
);  
int _fstat32i64(   
   int fd,  
   struct _stat32i64 *buffer   
);  
int _fstat64i32(   
   int fd,  
   struct _stat64i32 *buffer   
);  
```  
  
#### Parameters  
 `fd`  
 File descriptor of the open file.  
  
 `buffer`  
 Pointer to the structure to store results.  
  
## Return Value  
 Returns 0 if the file-status information is obtained. A return value of –1 indicates an error. If the file descriptor is invalid or `buffer` is `NULL`, the invalid parameter handler is invoked, as described in [Parameter Validation](../vs140/Parameter-Validation.md). If execution is allowed to continue, `errno` is set to `EBADF`, in the case of an invalid file descriptor, or to `EINVAL`, if `buffer` is `NULL`.  
  
## Remarks  
 The `_fstat` function obtains information about the open file associated with `fd` and stores it in the structure pointed to by `buffer`. The `_stat` structure, defined in SYS\Stat.h, contains the following fields.  
  
 `st_atime`  
 Time of the last file access.  
  
 `st_ctime`  
 Time of the creation of the file.  
  
 `st_dev`  
 If a device, `fd`; otherwise 0.  
  
 `st_mode`  
 Bit mask for file-mode information. The `_S_IFCHR` bit is set if `fd` refers to a device. The `_S_IFREG` bit is set if `fd` refers to an ordinary file. The read/write bits are set according to the file's permission mode. `_S_IFCHR` and other constants are defined in SYS\Stat.h.  
  
 `st_mtime`  
 Time of the last modification of the file.  
  
 `st_nlink`  
 Always 1 on non-NTFS file systems.  
  
 `st_rdev`  
 If a device, `fd`; otherwise 0.  
  
 `st_size`  
 Size of the file in bytes.  
  
 If `fd` refers to a device, the `st_atime`, `st_ctime`, `st_mtime`, and `st_size` fields are not meaningful.  
  
 Because Stat.h uses the [_dev_t](../vs140/Standard-Types.md) type, which is defined in Types.h, you must include Types.h before Stat.h in your code.  
  
 `_fstat64`, which uses the `__stat64` structure, allows file-creation dates to be expressed up through 23:59:59, December 31, 3000, UTC; whereas the other functions only represent dates through 23:59:59 January 18, 2038, UTC. Midnight, January 1, 1970, is the lower bound of the date range for all these functions.  
  
 Variations of these functions support 32-bit or 64-bit time types and 32-bit or 64-bit file lengths. The first numerical suffix (`32` or `64`) indicates the size of the time type used; the second suffix is either `i32` or `i64`, indicating whether the file size is represented as a 32-bit or 64-bit integer.  
  
 `_fstat` is equivalent to `_fstat64i32`, and `struct``_stat` contains a 64-bit time. This is true unless `_USE_32BIT_TIME_T` is defined, in which case the old behavior is in effect; `_fstat` uses a 32-bit time, and `struct``_stat` contains a 32-bit time. The same is true for `_fstati64`.  
  
### Time Type and File Length Type Variations of _stat  
  
|Functions|_USE_32BIT_TIME_T defined?|Time type|File length type|  
|---------------|------------------------------------|---------------|----------------------|  
|`_fstat`|Not defined|64-bit|32-bit|  
|`_fstat`|Defined|32-bit|32-bit|  
|`_fstat32`|Not affected by the macro definition|32-bit|32-bit|  
|`_fstat64`|Not affected by the macro definition|64-bit|64-bit|  
|`_fstati64`|Not defined|64-bit|64-bit|  
|`_fstati64`|Defined|32-bit|64-bit|  
|`_fstat32i64`|Not affected by the macro definition|32-bit|64-bit|  
|`_fstat64i32`|Not affected by the macro definition|64-bit|32-bit|  
  
## Requirements  
  
|Function|Required header|  
|--------------|---------------------|  
|`_fstat`|<sys/stat.h> and <sys/types.h>|  
|`_fstat32`|<sys/stat.h> and <sys/types.h>|  
|`_fstat64`|<sys/stat.h> and <sys/types.h>|  
|`_fstati64`|<sys/stat.h> and <sys/types.h>|  
|`_fstat32i64`|<sys/stat.h> and <sys/types.h>|  
|`_fstat64i32`|<sys/stat.h> and <sys/types.h>|  
  
 For more compatibility information, see [Compatibility](../vs140/Compatibility.md) in the Introduction.  
  
## Example  
  
```  
// crt_fstat.c  
// This program uses _fstat to report  
// the size of a file named F_STAT.OUT.  
  
#include <io.h>  
#include <fcntl.h>  
#include <time.h>  
#include <sys/types.h>  
#include <sys/stat.h>  
#include <stdio.h>  
#include <stdlib.h>  
#include <string.h>  
#include <errno.h>  
#include <share.h>  
  
int main( void )  
{  
   struct _stat buf;  
   int fd, result;  
   char buffer[] = "A line to output";  
   char timebuf[26];  
   errno_t err;  
  
   _sopen_s( &fd,  
             "f_stat.out",  
             _O_CREAT | _O_WRONLY | _O_TRUNC,  
             _SH_DENYNO,  
             _S_IREAD | _S_IWRITE );  
   if( fd != -1 )  
      _write( fd, buffer, strlen( buffer ) );  
  
   // Get data associated with "fd":   
   result = _fstat( fd, &buf );  
  
   // Check if statistics are valid:   
   if( result != 0 )  
   {  
      if (errno == EBADF)  
        printf( "Bad file descriptor.\n" );  
      else if (errno == EINVAL)  
        printf( "Invalid argument to _fstat.\n" );  
   }  
   else  
   {  
      printf( "File size     : %ld\n", buf.st_size );  
      err = ctime_s(timebuf, 26, &buf.st_mtime);  
      if (err)  
      {  
         printf("Invalid argument to ctime_s.");  
         exit(1);  
      }  
      printf( "Time modified : %s", timebuf );  
   }  
   _close( fd );  
}  
```  
  
 **File size     : 16**  
**Time modified : Wed May 07 15:25:11 2003**   
## .NET Framework Equivalent  
 Not applicable. To call the standard C function, use `PInvoke`. For more information, see [Platform Invoke Examples](assetId:///15926806-f0b7-487e-93a6-4e9367ec689f).  
  
## See Also  
 [File Handling](../Topic/File%20Handling.md)   
 [_access, _waccess](../Topic/_access,%20_waccess.md)   
 [_chmod, _wchmod](../vs140/_chmod--_wchmod.md)   
 [_filelength, _filelengthi64](../vs140/_filelength--_filelengthi64.md)   
 [_stat, _wstat Functions](../vs140/_stat--_stat32--_stat64--_stati64--_stat32i64--_stat64i32--_wstat--_wstat32--_wstat64--_wstati64--_wstat32i64--_wstat64i32.md)