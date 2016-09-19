---
title: "_umask_s"
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
  - _umask_s
apilocation: 
  - msvcr110.dll
  - msvcr100.dll
  - msvcrt.dll
  - msvcr120.dll
  - msvcr110_clr0400.dll
  - msvcr90.dll
  - msvcr80.dll
apitype: DLLExport
ms.assetid: 70898f61-bf2b-4d8d-8291-0ccaa6d33145
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _umask_s
Sets the default file-permission mask. A version of [_umask](../vs140/_umask.md) with security enhancements as described in [Security Enhancements in the CRT](../vs140/Security-Features-in-the-CRT.md).  
  
## Syntax  
  
```  
errno_t _umask_s(  
   int mode,  
   int * pOldMode  
);  
```  
  
#### Parameters  
 [in] `mode`  
 Default permission setting.  
  
 [out] `oldMode`  
 The previous value of the permission setting.  
  
## Return Value  
 Returns an error code if `Mode` does not specify a valid mode or the `pOldMode` pointer is `NULL`.  
  
### Error Conditions  
  
|`mode`|`pOldMode`|**Return Value**|**Contents of**  `oldMode`|  
|------------|----------------|----------------------|--------------------------------|  
|any|`NULL`|`EINVAL`|not modified|  
|invalid mode|any|`EINVAL`|not modified|  
  
 If one of the above conditions occurs, the invalid parameter handler is invoked, as described in [Parameter Validation](../vs140/Parameter-Validation.md). If execution is allowed to continue, `_umask_s` returns `EINVAL` and sets `errno` to `EINVAL`.  
  
## Remarks  
 The `_umask_s` function sets the file-permission mask of the current process to the mode specified by `mode`*.* The file-permission mask modifies the permission setting of new files created by `_creat`, `_open`, or `_sopen`. If a bit in the mask is 1, the corresponding bit in the file's requested permission value is set to 0 (disallowed). If a bit in the mask is 0, the corresponding bit is left unchanged. The permission setting for a new file is not set until the file is closed for the first time.  
  
 The integer expression `pmode` contains one or both of the following manifest constants, defined in SYS\STAT.H:  
  
 `_S_IWRITE`  
 Writing permitted.  
  
 `_S_IREAD`  
 Reading permitted.  
  
 `_S_IREAD | _S_IWRITE`  
 Reading and writing permitted.  
  
 When both constants are given, they are joined with the bitwise-OR operator ( `|` ). If the `mode` argument is `_S_IREAD`, reading is not allowed (the file is write-only). If the `mode` argument is `_S_IWRITE`, writing is not allowed (the file is read-only). For example, if the write bit is set in the mask, any new files will be read-only. Note that with MS-DOS and the Windows operating systems, all files are readable; it is not possible to give write-only permission. Therefore, setting the read bit with `_umask_s` has no effect on the file's modes.  
  
 If `pmode` is not a combination of one of the manifest constants or incorporates an alternate set of constants, the function will simply ignore those.  
  
## Requirements  
  
|Routine|Required header|  
|-------------|---------------------|  
|`_umask_s`|<io.h> and <sys/stat.h> and <sys/types.h>|  
  
 For additional compatibility information, see [Compatibility](../vs140/Compatibility.md) in the Introduction.  
  
## Example  
  
```  
// crt_umask_s.c  
/* This program uses _umask_s to set  
 * the file-permission mask so that all future  
 * files will be created as read-only files.  
 * It also displays the old mask.  
 */  
  
#include <sys/stat.h>  
#include <sys/types.h>  
#include <io.h>  
#include <stdio.h>  
  
int main( void )  
{  
   int oldmask, err;  
  
   /* Create read-only files: */  
   err = _umask_s( _S_IWRITE, &oldmask );  
   if (err)  
   {  
      printf("Error setting the umask.\n");  
      exit(1);  
   }  
   printf( "Oldmask = 0x%.4x\n", oldmask );  
}  
```  
  
 **Oldmask = 0x0000**   
## .NET Framework Equivalent  
 [System::IO::File::SetAttributes](https://msdn.microsoft.com/en-us/library/system.io.file.setattributes.aspx)  
  
## See Also  
 [File Handling](../Topic/File%20Handling.md)   
 [Low-Level I/O](../vs140/Low-Level-I-O.md)   
 [_chmod, _wchmod](../vs140/_chmod--_wchmod.md)   
 [_creat, _wcreat](../vs140/_creat--_wcreat.md)   
 [_mkdir, _wmkdir](../vs140/_mkdir--_wmkdir.md)   
 [_open, _wopen](../Topic/_open,%20_wopen.md)   
 [_umask](../vs140/_umask.md)