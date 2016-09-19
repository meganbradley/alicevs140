---
title: "_getmaxstdio"
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
  - _getmaxstdio
apilocation: 
  - msvcrt.dll
  - msvcr90.dll
  - msvcr100.dll
  - msvcr110_clr0400.dll
  - msvcr80.dll
  - msvcr110.dll
  - msvcr120.dll
apitype: DLLExport
ms.assetid: 700ca8ce-4a8c-4e00-9467-dfa9d6b831a0
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _getmaxstdio
Returns the number of simultaneously open files permitted at the stream I/O level.  
  
## Syntax  
  
```  
int _getmaxstdio( void );  
```  
  
## Return Value  
 Returns a number that represents the number of simultaneously open files currently permitted at the `stdio` level.  
  
## Remarks  
 Use [_setmaxstdio](../vs140/_setmaxstdio.md) to configure the number of simultaneously open files permitted at the `stdio` level.  
  
## Requirements  
  
|Routine|Required header|  
|-------------|---------------------|  
|`_getmaxstdio`|<stdio.h>|  
  
 For more compatibility information, see [Compatibility](../vs140/Compatibility.md) in the Introduction.  
  
## Example  
  
```  
// crt_setmaxstdio.c  
// The program retrieves the maximum number  
// of open files and prints the results  
// to the console.  
  
#include <stdio.h>  
  
int main()  
{  
   printf( "%d\n", _getmaxstdio());  
  
   _setmaxstdio(2048);  
  
   printf( "%d\n", _getmaxstdio());  
}  
```  
  
 **512**  
**2048**   
## .NET Framework Equivalent  
 Not applicable. To call the standard C function, use `PInvoke`. For more information, see [Platform Invoke Examples](assetId:///15926806-f0b7-487e-93a6-4e9367ec689f).  
  
## See Also  
 [Stream I/O](../vs140/Stream-I-O.md)