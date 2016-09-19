---
title: "_getcwd, _wgetcwd"
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
  - _wgetcwd
  - _getcwd
apilocation: 
  - msvcr120.dll
  - msvcr100.dll
  - msvcr90.dll
  - msvcrt.dll
  - msvcr80.dll
  - msvcr110.dll
  - msvcr110_clr0400.dll
apitype: DLLExport
ms.assetid: 888dc8c6-5595-4071-be55-816b38e3e739
caps.latest.revision: 24
translation.priority.mt: 
  - de-de
  - ja-jp
---
# _getcwd, _wgetcwd
Gets the current working directory.  
  
## Syntax  
  
```  
char *_getcwd(   
   char *buffer,  
   int maxlen   
);  
wchar_t *_wgetcwd(   
   wchar_t *buffer,  
   int maxlen   
);  
```  
  
#### Parameters  
 `buffer`  
 Storage location for the path.  
  
 `maxlen`  
 Maximum length of the path in characters: `char` for `_getcwd` and `wchar_t` for `_wgetcwd`.  
  
## Return Value  
 Returns a pointer to `buffer`. A `NULL` return value indicates an error, and `errno` is set either to `ENOMEM`, indicating that there is insufficient memory to allocate `maxlen` bytes (when a `NULL` argument is given as `buffer`), or to `ERANGE`, indicating that the path is longer than `maxlen` characters. If `maxlen` is less than or equal to zero, this function invokes an invalid parameter handler, as described in [Parameter Validation](../vs140/Parameter-Validation.md).  
  
 For more information about these and other return codes, see [_doserrno, errno, _sys_errlist, and _sys_nerr](../vs140/errno--_doserrno--_sys_errlist--and-_sys_nerr.md).  
  
## Remarks  
 The `_getcwd` function gets the full path of the current working directory for the default drive and stores it at `buffer`. The integer argument `maxlen` specifies the maximum length for the path. An error occurs if the length of the path (including the terminating null character) exceeds `maxlen`*.* The `buffer` argument can be `NULL`; a buffer of at least size `maxlen` (more only if necessary) is automatically allocated, using `malloc`, to store the path. This buffer can later be freed by calling `free` and passing it the `_getcwd` return value (a pointer to the allocated buffer).  
  
 `_getcwd` returns a string that represents the path of the current working directory. If the current working directory is the root, the string ends with a backslash ( `\` ). If the current working directory is a directory other than the root, the string ends with the directory name and not with a backslash.  
  
 `_wgetcwd` is a wide-character version of `_getcwd`; the `buffer` argument and return value of `_wgetcwd` are wide-character strings. `_wgetcwd` and `_getcwd` behave identically otherwise.  
  
 When `_DEBUG` and `_CRTDBG_MAP_ALLOC` are defined, calls to `_getcwd` and `_wgetcwd` are replaced by calls to `_getcwd_dbg` and `_wgetcwd_dbg` to allow for debugging memory allocations. For more information, see [_getcwd_dbg, _wgetcwd_dbg](../vs140/_getcwd_dbg--_wgetcwd_dbg.md).  
  
### Generic-Text Routine Mappings  
  
|Tchar.h routine|_UNICODE and _MBCS not defined|_MBCS defined|_UNICODE defined|  
|---------------------|--------------------------------------|--------------------|-----------------------|  
|`_tgetcwd`|`_getcwd`|`_getcwd`|`_wgetcwd`|  
  
## Requirements  
  
|Routine|Required header|  
|-------------|---------------------|  
|`_getcwd`|<direct.h>|  
|`_wgetcwd`|<direct.h> or <wchar.h>|  
  
 For more compatibility information, see [Compatibility](../vs140/Compatibility.md).  
  
## Example  
  
```  
// crt_getcwd.c  
// This program places the name of the current directory in the   
// buffer array, then displays the name of the current directory   
// on the screen. Passing NULL as the buffer forces getcwd to allocate  
// memory for the path, which allows the code to support file paths  
// longer than _MAX_PATH, which are supported by NTFS.  
  
#include <direct.h>  
#include <stdlib.h>  
#include <stdio.h>  
  
int main( void )  
{  
   char* buffer;  
  
   // Get the current working directory:   
   if( (buffer = _getcwd( NULL, 0 )) == NULL )  
      perror( "_getcwd error" );  
   else  
   {  
      printf( "%s \nLength: %d\n", buffer, strnlen(buffer) );  
      free(buffer);  
   }  
}  
```  
  
 **C:\Code**   
## .NET Framework Equivalent  
 [System::Environment::CurrentDirectory](https://msdn.microsoft.com/en-us/library/system.environment.currentdirectory.aspx)  
  
## See Also  
 [Directory Control](../vs140/Directory-Control.md)   
 [_chdir, _wchdir](../vs140/_chdir--_wchdir.md)   
 [_mkdir, _wmkdir](../vs140/_mkdir--_wmkdir.md)   
 [_rmdir, _wrmdir](../vs140/_rmdir--_wrmdir.md)