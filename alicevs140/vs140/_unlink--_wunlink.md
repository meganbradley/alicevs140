---
title: "_unlink, _wunlink"
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
  - _unlink
  - _wunlink
apilocation: 
  - msvcr100.dll
  - msvcr120.dll
  - msvcr80.dll
  - msvcr110.dll
  - msvcr110_clr0400.dll
  - msvcr90.dll
  - msvcrt.dll
apitype: DLLExport
ms.assetid: 5e4f5f1b-1e99-4391-9b18-9ac63c32fae8
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _unlink, _wunlink
Delete a file.  
  
## Syntax  
  
```  
int _unlink(  
   const char *filename   
);  
int _wunlink(  
   const wchar_t *filename   
);  
```  
  
#### Parameters  
 `filename`  
 Name of file to remove.  
  
## Return Value  
 Each of these functions returns 0 if successful. Otherwise, the function returns –1 and sets `errno` to `EACCES`, which means the path specifies a read-only file, or to `ENOENT`, which means the file or path is not found or the path specified a directory.  
  
 See [_doserrno, errno, _sys_errlist, and _sys_nerr](../vs140/errno--_doserrno--_sys_errlist--and-_sys_nerr.md) for more information on these, and other, return codes.  
  
## Remarks  
 The `_unlink` function deletes the file specified by `filename`. `_wunlink` is a wide-character version of `_unlink`; the `filename` argument to `_wunlink` is a wide-character string. These functions behave identically otherwise.  
  
### Generic-Text Routine Mappings  
  
|TCHAR.H routine|_UNICODE & _MBCS not defined|_MBCS defined|_UNICODE defined|  
|---------------------|------------------------------------|--------------------|-----------------------|  
|`_tunlink`|`_unlink`|`_unlink`|`_wunlink`|  
  
## Requirements  
  
|Routine|Required header|  
|-------------|---------------------|  
|`_unlink`|<io.h> and <stdio.h>|  
|`_wunlink`|<io.h> or <wchar.h>|  
  
 For additional compatibility information, see [Compatibility](../vs140/Compatibility.md) in the Introduction.  
  
## Code Example  
 This program uses _unlink to delete CRT_UNLINK.TXT.  
  
```  
// crt_unlink.c  
  
#include <stdio.h>  
  
int main( void )  
{  
   if( _unlink( "crt_unlink.txt" ) == -1 )  
      perror( "Could not delete 'CRT_UNLINK.TXT'" );  
   else  
      printf( "Deleted 'CRT_UNLINK.TXT'\n" );  
}  
```  
  
### Input: crt_unlink.txt  
  
```  
This file will be deleted.  
```  
  
### Sample Output  
  
```  
Deleted 'CRT_UNLINK.TXT'  
```  
  
## .NET Framework Equivalent  
 [System::IO::File::Delete](https://msdn.microsoft.com/en-us/library/system.io.file.delete.aspx)  
  
## See Also  
 [File Handling](../Topic/File%20Handling.md)   
 [_close](../vs140/_close.md)   
 [remove, _wremove](../vs140/remove--_wremove.md)