---
title: "_getdrive"
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
  - _getdrive
apilocation: 
  - msvcrt.dll
  - msvcr110.dll
  - msvcr120.dll
  - msvcr90.dll
  - msvcr100.dll
  - msvcr80.dll
  - msvcr110_clr0400.dll
apitype: DLLExport
ms.assetid: e40631a0-8f1a-4897-90ac-e1037ff30bca
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _getdrive
Gets the current disk drive.  
  
> [!IMPORTANT]
>  This API cannot be used in applications that execute in the Windows Runtime. For more information, see [CRT functions not supported with /ZW](http://msdn.microsoft.com/library/windows/apps/jj606124.aspx).  
  
## Syntax  
  
```  
int _getdrive( void );  
```  
  
## Return Value  
 Returns the current (default) drive (1=A, 2=B, and so on). There is no error return.  
  
## Requirements  
  
|Routine|Required header|  
|-------------|---------------------|  
|`_getdrive`|<direct.h>|  
  
 For more compatibility information, see [Compatibility](../vs140/Compatibility.md).  
  
## Example  
  
```  
// crt_getdrive.c  
// compile with: /c  
// Illustrates drive functions including:  
//    _getdrive       _chdrive        _getdcwd  
//  
  
#include <stdio.h>  
#include <direct.h>  
#include <stdlib.h>  
#include <ctype.h>  
  
int main( void )  
{  
   int ch, drive, curdrive;  
   static char path[_MAX_PATH];  
  
   // Save current drive.  
   curdrive = _getdrive();  
  
   printf( "Available drives are:\n" );  
  
   // If we can switch to the drive, it exists.  
   for( drive = 1; drive <= 26; drive++ )  
   {  
      if( !_chdrive( drive ) )  
      {  
         printf( "%c:", drive + 'A' - 1 );  
         if( _getdcwd( drive, path, _MAX_PATH ) != NULL )  
            printf( " (Current directory is %s)", path );  
         putchar( '\n' );  
      }  
   }  
  
   // Restore original drive.  
   _chdrive( curdrive );  
}  
```  
  
 **Available drives are:**  
**A: (Current directory is A:\\)**  
**C: (Current directory is C:\\)**  
**E: (Current directory is E:\testdir\bin)**  
**F: (Current directory is F:\\)**  
**G: (Current directory is G:\\)**   
## .NET Framework Equivalent  
 [System::Environment::CurrentDirectory](https://msdn.microsoft.com/en-us/library/system.environment.currentdirectory.aspx)  
  
## See Also  
 [Directory Control](../vs140/Directory-Control.md)   
 [_chdrive](../vs140/_chdrive.md)   
 [_getcwd, _wgetcwd](../vs140/_getcwd--_wgetcwd.md)   
 [_getdcwd, _wgetdcwd](../vs140/_getdcwd--_wgetdcwd.md)