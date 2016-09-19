---
title: "perror, _wperror"
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
  - _wperror
  - perror
apilocation: 
  - msvcr100.dll
  - msvcr110.dll
  - msvcr80.dll
  - msvcr110_clr0400.dll
  - msvcr90.dll
  - msvcr120.dll
  - msvcrt.dll
apitype: DLLExport
ms.assetid: 34fce792-16fd-4673-9849-cd88b54b6cd5
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# perror, _wperror
Print an error message.  
  
## Syntax  
  
```  
  
      void perror(  
   const char *string   
);  
void _wperror(  
   const wchar_t *string   
);  
```  
  
#### Parameters  
 `string`  
 String message to print.  
  
## Remarks  
 The `perror` function prints an error message to `stderr`. `_wperror` is a wide-character version of **_perror**; the `string` argument to `_wperror` is a wide-character string. `_wperror` and **_perror** behave identically otherwise.  
  
### Generic-Text Routine Mappings  
  
|TCHAR.H routine|_UNICODE & _MBCS not defined|_MBCS defined|_UNICODE defined|  
|---------------------|------------------------------------|--------------------|-----------------------|  
|`_tperror`|`perror`|`perror`|`_wperror`|  
  
 `string` is printed first, followed by a colon, then by the system error message for the last library call that produced the error, and finally by a newline character. If `string` is a null pointer or a pointer to a null string, `perror` prints only the system error message.  
  
 The error number is stored in the variable [errno](../vs140/errno--_doserrno--_sys_errlist--and-_sys_nerr.md) (defined in ERRNO.H). The system error messages are accessed through the variable [_sys_errlist](../vs140/errno--_doserrno--_sys_errlist--and-_sys_nerr.md), which is an array of messages ordered by error number. `perror` prints the appropriate error message using the `errno` value as an index to `_sys_errlist`. The value of the variable [_sys_nerr](../vs140/errno--_doserrno--_sys_errlist--and-_sys_nerr.md) is defined as the maximum number of elements in the `_sys_errlist` array.  
  
 For accurate results, call `perror` immediately after a library routine returns with an error. Otherwise, subsequent calls can overwrite the `errno` value.  
  
 In the Windows operating system, some `errno` values listed in ERRNO.H are unused. These values are reserved for use by the UNIX operating system. See [_doserrno, errno, _sys_errlist, and _sys_nerr](../vs140/errno--_doserrno--_sys_errlist--and-_sys_nerr.md) for a listing of `errno` values used by the Windows operating system. `perror` prints an empty string for any `errno` value not used by these platforms.  
  
## Requirements  
  
|Routine|Required header|  
|-------------|---------------------|  
|`perror`|<stdio.h> or <stdlib.h>|  
|`_wperror`|<stdio.h> or <wchar.h>|  
  
 For additional compatibility information, see [Compatibility](../vs140/Compatibility.md) in the Introduction.  
  
## Libraries  
 All versions of the [C run-time libraries](../vs140/CRT-Library-Features.md).  
  
## Example  
  
```  
// crt_perror.c  
// compile with: /W3  
/* This program attempts to open a file named  
 * NOSUCHF.ILE. Because this file probably doesn't exist,  
 * an error message is displayed. The same message is  
 * created using perror, strerror, and _strerror.  
 */  
  
#include <fcntl.h>  
#include <sys/types.h>  
#include <sys/stat.h>  
#include <io.h>  
#include <stdlib.h>  
#include <stdio.h>  
#include <string.h>  
#include <share.h>  
  
int main( void )  
{  
   int  fh;  
  
   if( _sopen_s( &fh, "NOSUCHF.ILE", _O_RDONLY, _SH_DENYNO, 0 ) != 0 )  
   {  
      /* Three ways to create error message: */  
      perror( "perror says open failed" );  
      printf( "strerror says open failed: %s\n",  
         strerror( errno ) ); // C4996  
      printf( _strerror( "_strerror says open failed" ) ); // C4996  
      // Note: strerror and _strerror are deprecated; consider  
      // using strerror_s and _strerror_s instead.  
   }  
   else  
   {  
      printf( "open succeeded on input file\n" );  
      _close( fh );  
   }  
}  
```  
  
## Output  
  
```  
perror says open failed: No such file or directory  
strerror says open failed: No such file or directory  
_strerror says open failed: No such file or directory  
```  
  
## .NET Framework Equivalent  
 Not applicable. To call the standard C function, use `PInvoke`. For more information, see [Platform Invoke Examples](assetId:///15926806-f0b7-487e-93a6-4e9367ec689f).  
  
## See Also  
 [Process and Environment Control](../vs140/Process-and-Environment-Control.md)   
 [clearerr](../vs140/clearerr.md)   
 [ferror](../vs140/ferror.md)   
 [strerror, _strerror, _wcserror, \__wcserror](../vs140/strerror--_strerror--_wcserror--__wcserror.md)