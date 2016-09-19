---
title: "_rmdir, _wrmdir"
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
  - _wrmdir
  - _rmdir
apilocation: 
  - msvcr100.dll
  - msvcr90.dll
  - msvcr110.dll
  - msvcrt.dll
  - msvcr120.dll
  - msvcr80.dll
  - msvcr110_clr0400.dll
apitype: DLLExport
ms.assetid: 652c2a5a-b0ac-4493-864e-1edf484333c5
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _rmdir, _wrmdir
Deletes a directory.  
  
## Syntax  
  
```  
  
      int _rmdir(  
   const char *dirname   
);  
int _wrmdir(  
   const wchar_t *dirname   
);  
```  
  
#### Parameters  
 `dirname`  
 Path of the directory to be removed.  
  
## Return Value  
 Each of these functions returns 0 if the directory is successfully deleted. A return value of –1 indicates an error and `errno` is set to one of the following values:  
  
 **ENOTEMPTY**  
 Given path is not a directory, the directory is not empty, or the directory is either the current working directory or the root directory.  
  
 `ENOENT`  
 Path is invalid.  
  
 **EACCES**  
 A program has an open handle to the directory.  
  
 For more information about these and other return codes, see [_doserrno, errno, _sys_errlist, and _sys_nerr](../vs140/errno--_doserrno--_sys_errlist--and-_sys_nerr.md).  
  
## Remarks  
 The `_rmdir` function deletes the directory specified by `dirname`. The directory must be empty, and it must not be the current working directory or the root directory.  
  
 `_wrmdir` is a wide-character version of `_rmdir`; the `dirname` argument to `_wrmdir` is a wide-character string. `_wrmdir` and `_rmdir` behave identically otherwise.  
  
### Generic-Text Routine Mappings  
  
|Tchar.h routine|_UNICODE and _MBCS not defined|_MBCS defined|_UNICODE defined|  
|---------------------|--------------------------------------|--------------------|-----------------------|  
|`_trmdir`|`_rmdir`|`_rmdir`|`_wrmdir`|  
  
## Requirements  
  
|Routine|Required header|  
|-------------|---------------------|  
|`_rmdir`|<direct.h>|  
|`_wrmdir`|<direct.h> or <wchar.h>|  
  
 For more compatibility information, see [Compatibility](../vs140/Compatibility.md) in the Introduction.  
  
## Libraries  
 All versions of the [C run-time libraries](../vs140/CRT-Library-Features.md).  
  
## Example  
 See the example for [_mkdir](../vs140/_mkdir--_wmkdir.md).  
  
## .NET Framework Equivalent  
 [System::IO::Directory::Delete](https://msdn.microsoft.com/en-us/library/system.io.directory.delete.aspx)  
  
## See Also  
 [Directory Control](../vs140/Directory-Control.md)   
 [_chdir, _wchdir](../vs140/_chdir--_wchdir.md)   
 [_mkdir, _wmkdir](../vs140/_mkdir--_wmkdir.md)