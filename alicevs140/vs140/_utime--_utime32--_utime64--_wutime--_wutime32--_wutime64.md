---
title: "_utime, _utime32, _utime64, _wutime, _wutime32, _wutime64"
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
  - _utime64
  - _utime
  - _wutime
  - _wutime64
  - _wutime32
  - _utime32
apilocation: 
  - msvcr110_clr0400.dll
  - msvcr100.dll
  - msvcr80.dll
  - msvcrt.dll
  - msvcr120.dll
  - msvcr90.dll
  - msvcr110.dll
apitype: DLLExport
ms.assetid: 8d482d40-19b9-4591-bfee-5d7f601d1a9e
caps.latest.revision: 18
translation.priority.mt: 
  - de-de
  - ja-jp
---
# _utime, _utime32, _utime64, _wutime, _wutime32, _wutime64
Set the file modification time.  
  
## Syntax  
  
```  
int _utime(  
   const char *filename,  
   struct _utimbuf *times   
);  
int _utime32(  
   const char *filename,  
   struct __utimbuf32 *times   
);  
int _utime64(  
   const char *filename,  
   struct __utimbuf64 *times   
);  
int _wutime(  
   const wchar_t *filename,  
   struct _utimbuf *times   
);  
int _wutime32(  
   const wchar_t *filename,  
   struct __utimbuf32 *times   
);  
int _wutime64(  
   const wchar_t *filename,  
   struct __utimbuf64 *times   
);  
```  
  
#### Parameters  
 `filename`  
 Pointer to a string that contains the path or filename.  
  
 `times`  
 Pointer to stored time values.  
  
## Return Value  
 Each of these functions returns 0 if the file-modification time was changed. A return value of –1 indicates an error. If an invalid parameter is passed, the invalid parameter handler is invoked, as described in [Parameter Validation](../vs140/Parameter-Validation.md). If execution is allowed to continue, these functions return -1 and `errno` is set to one of the following values:  
  
 `EACCES`  
 Path specifies directory or read-only file  
  
 `EINVAL`  
 Invalid `times` argument  
  
 `EMFILE`  
 Too many open files (the file must be opened to change its modification time)  
  
 `ENOENT`  
 Path or filename not found  
  
 See [_doserrno, errno, _sys_errlist, and _sys_nerr](../vs140/errno--_doserrno--_sys_errlist--and-_sys_nerr.md) for more information on these, and other, return codes.  
  
 The date can be changed for a file if the change date is after midnight, January 1, 1970, and before the end date of the function used. `_utime` and `_wutime` use a 64-bit time value, so the end date is 23:59:59, December 31, 3000, UTC. If `_USE_32BIT_TIME_T` is defined to force the old behavior, the end date is 23:59:59 January 18, 2038, UTC. `_utime32` or `_wutime32` use a 32-bit time type regardless of whether `_USE_32BIT_TIME_T` is defined, and always have the earlier end date. `_utime64` or `_wutime64` always use the 64-bit time type, so these functions always support the later end date.  
  
## Remarks  
 The `_utime` function sets the modification time for the file specified by `filename`*.* The process must have write access to the file in order to change the time. In the Windows operating system, you can change the access time and the modification time in the `_utimbuf` structure. If `times` is a `NULL` pointer, the modification time is set to the current local time. Otherwise, `times` must point to a structure of type `_utimbuf`, defined in SYS\UTIME.H.  
  
 The `_utimbuf` structure stores file access and modification times used by `_utime` to change file-modification dates. The structure has the following fields, which are both of type `time_t`:  
  
 `actime`  
 Time of file access  
  
 `modtime`  
 Time of file modification  
  
 Specific versions of the `_utimbuf` structure (`_utimebuf32` and `__utimbuf64`) are defined using the 32-bit and 64-bit versions of the time type. These are used in the 32-bit and 64-bit specific versions of this function. `_utimbuf` itself by default uses a 64-bit time type unless `_USE_32BIT_TIME_T` is defined.  
  
 `_utime` is identical to `_futime` except that the `filename` argument of `_utime` is a filename or a path to a file, rather than a file descriptor of an open file.  
  
 `_wutime` is a wide-character version of `_utime`; the `filename` argument to `_wutime` is a wide-character string. These functions behave identically otherwise.  
  
### Generic-Text Routine Mappings  
  
|TCHAR.H routine|_UNICODE & _MBCS not defined|_MBCS defined|_UNICODE defined|  
|---------------------|------------------------------------|--------------------|-----------------------|  
|`_tutime`|`_utime`|`_utime`|`_wutime`|  
|`_tutime32`|`_utime32`|`_utime32`|`_wutime32`|  
|`_tutime64`|`_utime64`|`_utime64`|`_wutime64`|  
  
## Requirements  
  
|Routine|Required headers|Optional headers|  
|-------------|----------------------|----------------------|  
|`_utime`, `_utime32`, `_utime64`|<sys/utime.h>|<errno.h>|  
|`_utime64`|<sys/utime.h>|<errno.h>|  
|`_wutime`|<utime.h> or <wchar.h>|<errno.h>|  
  
 For additional compatibility information, see [Compatibility](../vs140/Compatibility.md) in the Introduction.  
  
## Example  
 This program uses `_utime` to set the file-modification time to the current time.  
  
```  
// crt_utime.c  
#include <stdio.h>  
#include <stdlib.h>  
#include <sys/types.h>  
#include <sys/utime.h>  
#include <time.h>  
  
int main( void )  
{  
   struct tm tma = {0}, tmm = {0};  
   struct _utimbuf ut;  
  
   // Fill out the accessed time structure  
   tma.tm_hour = 12;  
   tma.tm_isdst = 0;  
   tma.tm_mday = 15;  
   tma.tm_min = 0;  
   tma.tm_mon = 0;  
   tma.tm_sec = 0;  
   tma.tm_year = 103;  
  
   // Fill out the modified time structure  
   tmm.tm_hour = 12;  
   tmm.tm_isdst = 0;  
   tmm.tm_mday = 15;  
   tmm.tm_min = 0;  
   tmm.tm_mon = 0;  
   tmm.tm_sec = 0;  
   tmm.tm_year = 102;  
  
   // Convert tm to time_t  
   ut.actime = mktime(&tma);  
   ut.modtime = mktime(&tmm);  
  
   // Show file time before and after  
   system( "dir crt_utime.c" );  
   if( _utime( "crt_utime.c", &ut ) == -1 )  
      perror( "_utime failed\n" );  
   else  
      printf( "File time modified\n" );  
   system( "dir crt_utime.c" );  
}  
```  
  
## Sample Output  
  
```  
Volume in drive C has no label.  
 Volume Serial Number is 9CAC-DE74  
  
 Directory of C:\test  
  
01/09/2003  05:38 PM               935 crt_utime.c  
               1 File(s)            935 bytes  
               0 Dir(s)  20,742,955,008 bytes free  
File time modified  
 Volume in drive C has no label.  
 Volume Serial Number is 9CAC-DE74  
  
 Directory of C:\test  
  
01/15/2002  12:00 PM               935 crt_utime.c  
               1 File(s)            935 bytes  
               0 Dir(s)  20,742,955,008 bytes free  
```  
  
## .NET Framework Equivalent  
 Not applicable. To call the standard C function, use `PInvoke`. For more information, see [Platform Invoke Examples](assetId:///15926806-f0b7-487e-93a6-4e9367ec689f).  
  
## See Also  
 [Time Management](../vs140/Time-Management.md)   
 [asctime, _wasctime](../vs140/asctime--_wasctime.md)   
 [ctime, _ctime32, _ctime64, _wctime, _wctime32, _wctime64](../vs140/ctime--_ctime32--_ctime64--_wctime--_wctime32--_wctime64.md)   
 [_fstat, _fstat32, _fstat64, _fstati64, _fstat32i64, _fstat64i32](../vs140/_fstat--_fstat32--_fstat64--_fstati64--_fstat32i64--_fstat64i32.md)   
 [_ftime, _ftime32, _ftime64](../vs140/_ftime--_ftime32--_ftime64.md)   
 [_futime, _futime32, _futime64](../vs140/_futime--_futime32--_futime64.md)   
 [gmtime, _gmtime32, _gmtime64](../vs140/gmtime--_gmtime32--_gmtime64.md)   
 [localtime, _localtime32, _localtime64](../vs140/localtime--_localtime32--_localtime64.md)   
 [_stat, _wstat Functions](../vs140/_stat--_stat32--_stat64--_stati64--_stat32i64--_stat64i32--_wstat--_wstat32--_wstat64--_wstati64--_wstat32i64--_wstat64i32.md)   
 [time, _time32, _time64](../vs140/time--_time32--_time64.md)