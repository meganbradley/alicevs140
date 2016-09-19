---
title: "_getdcwd, _wgetdcwd"
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
  - _getdcwd
  - _wgetdcwd
apilocation: 
  - msvcr110.dll
  - msvcr80.dll
  - msvcr120.dll
  - msvcr90.dll
  - msvcr100.dll
  - msvcr110_clr0400.dll
  - msvcrt.dll
apitype: DLLExport
ms.assetid: 184152f5-c7b0-495b-918d-f9a6adc178bd
caps.latest.revision: 26
translation.priority.mt: 
  - de-de
  - ja-jp
---
# _getdcwd, _wgetdcwd
Gets the full path of the current working directory on the specified drive.  
  
## Syntax  
  
```  
char *_getdcwd(   
   int drive,  
   char *buffer,  
   int maxlen   
);  
wchar_t *_wgetdcwd(   
   int drive,  
   wchar_t *buffer,  
   int maxlen   
);  
```  
  
#### Parameters  
 `drive`  
 A non-negative integer that specifies the drive (0 = default drive, 1 = A, 2 = B, and so on).  
  
 If the specified drive is not available, or the kind of drive (for example, removable, fixed, CD-ROM, RAM disk, or network drive) cannot be determined, the invalid-parameter handler, which is described in [Parameter Validation](../vs140/Parameter-Validation.md), is invoked.  
  
 `buffer`  
 Storage location for the path, or **NULL**.  
  
 If **NULL** is specified, this function allocates a buffer of at least `maxlen` size by using **malloc**, and the return value of `_getdcwd` is a pointer to the allocated buffer. The buffer can be freed by calling `free` and passing it the pointer.  
  
 `maxlen`  
 A nonzero positive integer that specifies the maximum length of the path, in characters: `char` for `_getdcwd` and `wchar_t` for `_wgetdcwd`.  
  
 If `maxlen` is not greater than zero, the invalid-parameter handler, which is described in [Parameter Validation](../vs140/Parameter-Validation.md), is invoked.  
  
## Return Value  
 Pointer to a string that represents the full path of the current working directory on the specified drive, or `NULL`, which indicates an error.  
  
 If `buffer` is specified as `NULL` and there is insufficient memory to allocate `maxlen` characters, an error occurs and `errno` is set to `ENOMEM`. If the length of the path,  which includes the terminating null character, exceeds `maxlen`, an error occurs and `errno` is set to `ERANGE`. For more information about these error codes, see [errno, _doserrno, _sys_errlist, and _sys_nerr](../vs140/errno--_doserrno--_sys_errlist--and-_sys_nerr.md).  
  
## Remarks  
 The `_getdcwd` function gets the full path of the current working directory on the specified drive and stores it at `buffer`. If the current working directory is set to the root, the string ends with a backslash (\\). If the current working directory is set to a directory other than the root, the string ends with the name of the directory and not with a backslash.  
  
 `_wgetdcwd` is a wide-character version of `_getdcwd`, and its `buffer` parameter and return value are wide-character strings. Otherwise, `_wgetdcwd` and `_getdcwd` behave identically.  
  
 This function is thread-safe even though it depends on **GetFullPathName**, which is itself not thread-safe. However, you can violate thread safety if your multithreaded application calls both this function and **GetFullPathName**. For more information, go to [MSDN Library](http://go.microsoft.com/fwlink/?LinkID=150542) and then search for **GetFullPathName**.  
  
 The version of this function that has the `_nolock` suffix behaves identically to this function except that it is not thread-safe and is not protected from interference by other threads. For more information, see [_getdcwd_nolock, _wgetdcwd_nolock](../vs140/_getdcwd_nolock--_wgetdcwd_nolock.md).  
  
 When `_DEBUG` and `_CRTDBG_MAP_ALLOC` are defined, calls to `_getdcwd` and `_wgetdcwd` are replaced by calls to `_getdcwd_dbg` and `_wgetdcwd_dbg` so that you can debug memory allocations. For more information, see[_getdcwd_dbg, _wgetdcwd_dbg](../Topic/_getdcwd_dbg,%20_wgetdcwd_dbg.md).  
  
### Generic-Text Routine Mappings  
  
|Tchar.h routine|_UNICODE and _MBCS not defined|_MBCS defined|_UNICODE defined|  
|---------------------|--------------------------------------|--------------------|-----------------------|  
|`_tgetdcwd`|`_getdcwd`|`_getdcwd`|`_wgetdcwd`|  
  
## Requirements  
  
|Routine|Required header|  
|-------------|---------------------|  
|`_getdcwd`|<direct.h>|  
|`_wgetdcwd`|<direct.h> or <wchar.h>|  
  
 For more compatibility information, see [Compatibility](../vs140/Compatibility.md).  
  
## Example  
 See the example in [_getdrive](../vs140/_getdrive.md).  
  
## .NET Framework Equivalent  
 [System::Environment::CurrentDirectory](https://msdn.microsoft.com/en-us/library/system.environment.currentdirectory.aspx)  
  
## See Also  
 [Directory Control](../vs140/Directory-Control.md)   
 [_chdir, _wchdir](../vs140/_chdir--_wchdir.md)   
 [_getcwd, _wgetcwd](../vs140/_getcwd--_wgetcwd.md)   
 [_getdrive](../vs140/_getdrive.md)   
 [_mkdir, _wmkdir](../vs140/_mkdir--_wmkdir.md)   
 [_rmdir, _wrmdir](../vs140/_rmdir--_wrmdir.md)