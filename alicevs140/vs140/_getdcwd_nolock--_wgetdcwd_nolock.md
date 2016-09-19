---
title: "_getdcwd_nolock, _wgetdcwd_nolock"
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
  - _wgetdcwd_nolock
  - _getdcwd_nolock
apilocation: 
  - msvcr100.dll
  - msvcr110_clr0400.dll
  - msvcr80.dll
  - msvcr120.dll
  - msvcr110.dll
  - msvcr90.dll
  - msvcrt.dll
apitype: DLLExport
ms.assetid: d9bdf712-43f8-4173-8f9a-844e82beaa97
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _getdcwd_nolock, _wgetdcwd_nolock
Gets the full path of the current working directory on the specified drive.  
  
> [!IMPORTANT]
>  This API cannot be used in applications that execute in the Windows Runtime. For more information, see [CRT functions not supported with /ZW](http://msdn.microsoft.com/library/windows/apps/jj606124.aspx).  
  
## Syntax  
  
```  
char *_getdcwd_nolock(   
   int drive,  
   char *buffer,  
   int maxlen   
);  
wchar_t *_wgetdcwd_nolock(   
   int drive,  
   wchar_t *buffer,  
   int maxlen   
);  
```  
  
#### Parameters  
 `drive`  
 Disk drive.  
  
 `buffer`  
 Storage location for the path.  
  
 `maxlen`  
 Maximum length of path in characters: `char` for `_getdcwd` and `wchar_t` for `_wgetdcwd`.  
  
## Return Value  
 See [_getdcwd, _wgetdcwd, _getdcwd_nolock, _wgetdcwd_nolock](../vs140/_getdcwd--_wgetdcwd.md).  
  
## Remarks  
 `_getdcwd_nolock` and `_wgetdcwd_nolock` are identical to `_getdcwd` and `_wgetdcwd`, respectively, except that they are not protected from interference by other threads. They might be faster because they do not incur the overhead of locking out other threads. Use these functions only in thread-safe contexts such as single-threaded applications or where the calling scope already handles thread isolation.  
  
### Generic-Text Routine Mappings  
  
|Tchar.h routine|_UNICODE and _MBCS not defined|_MBCS defined|_UNICODE defined|  
|---------------------|--------------------------------------|--------------------|-----------------------|  
|`_tgetdcwd_nolock`|`_getdcwd_nolock`|`_getdcwd_nolock`|`_wgetdcwd_nolock`|  
  
## Requirements  
  
|Routine|Required header|  
|-------------|---------------------|  
|`_getdcwd_nolock`|<direct.h>|  
|`_wgetdcwd_nolock`|<direct.h> or <wchar.h>|  
  
 For more compatibility information, see [Compatibility](../vs140/Compatibility.md).  
  
## .NET Framework Equivalent  
 [System::Environment::CurrentDirectory](https://msdn.microsoft.com/en-us/library/system.environment.currentdirectory.aspx)  
  
## See Also  
 [Directory Control](../vs140/Directory-Control.md)   
 [_chdir, _wchdir](../vs140/_chdir--_wchdir.md)   
 [_getcwd, _wgetcwd](../vs140/_getcwd--_wgetcwd.md)   
 [_getdrive](../vs140/_getdrive.md)   
 [_mkdir, _wmkdir](../vs140/_mkdir--_wmkdir.md)   
 [_rmdir, _wrmdir](../vs140/_rmdir--_wrmdir.md)