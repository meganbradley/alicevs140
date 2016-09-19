---
title: "_mkdir, _wmkdir"
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
  - _wmkdir
  - _mkdir
apilocation: 
  - msvcr110.dll
  - msvcr100.dll
  - msvcr120.dll
  - msvcr90.dll
  - msvcrt.dll
  - msvcr80.dll
  - msvcr110_clr0400.dll
apitype: DLLExport
ms.assetid: 7f22d01d-63a5-4712-a6e7-d34878b2d840
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _mkdir, _wmkdir
Creates a new directory.  
  
## Syntax  
  
```  
  
      int _mkdir(  
   const char *dirname   
);  
int _wmkdir(  
   const wchar_t *dirname   
);  
```  
  
#### Parameters  
 `dirname`  
 Path for a new directory.  
  
## Return Value  
 Each of these functions returns the value 0 if the new directory was created. On an error, the function returns –1 and sets `errno` as follows.  
  
 `EEXIST`  
 Directory was not created because `dirname` is the name of an existing file, directory, or device.  
  
 `ENOENT`  
 Path was not found.  
  
 For more information about these and other return codes, see [_doserrno, errno, _sys_errlist, and _sys_nerr](../vs140/errno--_doserrno--_sys_errlist--and-_sys_nerr.md).  
  
## Remarks  
 The `_mkdir` function creates a new directory with the specified *dirname.* `_mkdir` can create only one new directory per call, so only the last component of `dirname` can name a new directory. `_mkdir` does not translate path delimiters. In Windows NT, both the backslash ( \\) and the forward slash (/ ) are valid path delimiters in character strings in run-time routines.  
  
 `_wmkdir` is a wide-character version of `_mkdir`; the `dirname` argument to `_wmkdir` is a wide-character string. `_wmkdir` and `_mkdir` behave identically otherwise.  
  
### Generic-Text Routine Mappings  
  
|Tchar.h routine|_UNICODE and _MBCS not defined|_MBCS defined|_UNICODE defined|  
|---------------------|--------------------------------------|--------------------|-----------------------|  
|`_tmkdir`|`_mkdir`|`_mkdir`|`_wmkdir`|  
  
## Requirements  
  
|Routine|Required header|  
|-------------|---------------------|  
|`_mkdir`|<direct.h>|  
|`_wmkdir`|<direct.h> or <wchar.h>|  
  
 For more compatibility information, see [Compatibility](../vs140/Compatibility.md) in the Introduction.  
  
## Libraries  
 All versions of the [C run-time libraries](../vs140/CRT-Library-Features.md).  
  
## Example  
  
```  
// crt_makedir.c  
  
#include <direct.h>  
#include <stdlib.h>  
#include <stdio.h>  
  
int main( void )  
{  
   if( _mkdir( "\\testtmp" ) == 0 )  
   {  
      printf( "Directory '\\testtmp' was successfully created\n" );  
      system( "dir \\testtmp" );  
      if( _rmdir( "\\testtmp" ) == 0 )  
        printf( "Directory '\\testtmp' was successfully removed\n"  );  
      else  
         printf( "Problem removing directory '\\testtmp'\n" );  
   }  
   else  
      printf( "Problem creating directory '\\testtmp'\n" );  
}  
```  
  
## Sample Output  
  
```  
Directory '\testtmp' was successfully created  
 Volume in drive C has no label.  
 Volume Serial Number is E078-087A  
  
 Directory of C:\testtmp  
  
02/12/2002  09:56a      <DIR>          .  
02/12/2002  09:56a      <DIR>          ..  
               0 File(s)              0 bytes  
               2 Dir(s)  15,498,690,560 bytes free  
Directory '\testtmp' was successfully removed  
```  
  
## .NET Framework Equivalent  
  
-   [System::IO::Directory::CreateDirectory](https://msdn.microsoft.com/en-us/library/system.io.directory.createdirectory.aspx)  
  
-   [System::IO::DirectoryInfo::CreateSubdirectory](https://msdn.microsoft.com/en-us/library/system.io.directoryinfo.createsubdirectory.aspx)  
  
## See Also  
 [Directory Control](../vs140/Directory-Control.md)   
 [_chdir, _wchdir](../vs140/_chdir--_wchdir.md)   
 [_rmdir, _wrmdir](../vs140/_rmdir--_wrmdir.md)