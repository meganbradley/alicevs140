---
title: "rename, _wrename"
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
  - rename
  - _wrename
apilocation: 
  - msvcrt.dll
  - msvcr110_clr0400.dll
  - msvcr120.dll
  - msvcr90.dll
  - msvcr100.dll
  - msvcr80.dll
  - msvcr110.dll
apitype: DLLExport
ms.assetid: 9f0a6103-26a2-4dda-b14b-79a48946266a
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# rename, _wrename
Rename a file or directory.  
  
## Syntax  
  
```  
  
      int rename(  
   const char *oldname,  
   const char *newname   
);  
int _wrename(  
   const wchar_t *oldname,  
   const wchar_t *newname   
);  
```  
  
#### Parameters  
 *oldname*  
 Pointer to old name.  
  
 *newname*  
 Pointer to new name.  
  
## Return Value  
 Each of these functions returns 0 if it is successful. On an error, the function returns a nonzero value and sets `errno` to one of the following values:  
  
 `EACCES`  
 File or directory specified by *newname* already exists or could not be created (invalid path); or *oldname* is a directory and *newname* specifies a different path.  
  
 `ENOENT`  
 File or path specified by *oldname* not found.  
  
 `EINVAL`  
 Name contains invalid characters.  
  
 For other possible return values, see [_doserrno, _errno, syserrlist, and _sys_nerr](../vs140/errno--_doserrno--_sys_errlist--and-_sys_nerr.md).  
  
## Remarks  
 The **rename** function renames the file or directory specified by *oldname* to the name given by *newname*. The old name must be the path of an existing file or directory. The new name must not be the name of an existing file or directory. You can use **rename** to move a file from one directory or device to another by giving a different path in the *newname* argument. However, you cannot use **rename** to move a directory. Directories can be renamed, but not moved.  
  
 `_wrename` is a wide-character version of **_rename**; the arguments to `_wrename` are wide-character strings. `_wrename` and **_rename** behave identically otherwise.  
  
### Generic-Text Routine Mappings  
  
|TCHAR.H routine|_UNICODE & _MBCS not defined|_MBCS defined|_UNICODE defined|  
|---------------------|------------------------------------|--------------------|-----------------------|  
|`_trename`|**rename**|**rename**|`_wrename`|  
  
## Requirements  
  
|Routine|Required header|  
|-------------|---------------------|  
|**rename**|<io.h> or <stdio.h>|  
|`_wrename`|<stdio.h> or <wchar.h>|  
  
 For additional compatibility information, see [Compatibility](../vs140/Compatibility.md) in the Introduction.  
  
## Libraries  
 All versions of the [C run-time libraries](../vs140/CRT-Library-Features.md).  
  
## Example  
  
```  
// crt_renamer.c  
/* This program attempts to rename a file named  
 * CRT_RENAMER.OBJ to CRT_RENAMER.JBO. For this operation  
 * to succeed, a file named CRT_RENAMER.OBJ must exist and  
 * a file named CRT_RENAMER.JBO must not exist.  
 */  
  
#include <stdio.h>  
  
int main( void )  
{  
   int  result;  
   char old[] = "CRT_RENAMER.OBJ", new[] = "CRT_RENAMER.JBO";  
  
   /* Attempt to rename file: */  
   result = rename( old, new );  
   if( result != 0 )  
      printf( "Could not rename '%s'\n", old );  
   else  
      printf( "File '%s' renamed to '%s'\n", old, new );  
}  
```  
  
## Output  
  
```  
File 'CRT_RENAMER.OBJ' renamed to 'CRT_RENAMER.JBO'  
```  
  
## .NET Framework Equivalent  
 [System::IO::File::Move](https://msdn.microsoft.com/en-us/library/system.io.file.move.aspx)  
  
## See Also  
 [File Handling](../Topic/File%20Handling.md)