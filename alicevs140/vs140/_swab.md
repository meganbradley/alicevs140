---
title: "_swab"
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
  - _swab
apilocation: 
  - msvcr120.dll
  - msvcr110.dll
  - msvcr80.dll
  - msvcrt.dll
  - msvcr110_clr0400.dll
  - msvcr100.dll
  - msvcr90.dll
apitype: DLLExport
ms.assetid: 017142f2-050c-4f6a-8b49-6b094f58ec94
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _swab
Swaps bytes.  
  
## Syntax  
  
```  
void _swab(  
   char *src,  
   char *dest,  
   int n   
);  
```  
  
#### Parameters  
 `src`  
 Data to be copied and swapped.  
  
 `dest`  
 Storage location for swapped data.  
  
 `n`  
 Number of bytes to be copied and swapped.  
  
## Remarks  
 If `n` is even, the `_swab` function copies `n` bytes from `src`, swaps each pair of adjacent bytes, and stores the result at `dest`. If `n` is odd, `_swab` copies and swaps the first `n-1` bytes of `src`. `_swab` is typically used to prepare binary data for transfer to a machine that uses a different byte order.  
  
## Requirements  
  
|Routine|Required header|  
|-------------|---------------------|  
|`_swab`|<stdlib.h>|  
  
 For additional compatibility information, see [Compatibility](../vs140/Compatibility.md) in the Introduction.  
  
## Example  
  
```  
// crt_swab.c  
  
#include <stdlib.h>  
#include <stdio.h>  
  
char from[] = "BADCFEHGJILKNMPORQTSVUXWZY";  
char to[] =   "..........................";  
  
int main()  
{  
    printf( "Before: %s\n        %s\n\n", from, to );  
    _swab( from, to, sizeof( from ) );  
    printf( "After:  %s\n        %s\n\n", from, to );  
}  
```  
  
 **Before: BADCFEHGJILKNMPORQTSVUXWZY**  
 **..........................**  
**After:  BADCFEHGJILKNMPORQTSVUXWZY**  
 **ABCDEFGHIJKLMNOPQRSTUVWXYZ**   
## .NET Framework Equivalent  
 Not applicable. To call the standard C function, use `PInvoke`. For more information, see [Platform Invoke Examples](assetId:///15926806-f0b7-487e-93a6-4e9367ec689f).  
  
## See Also  
 [Buffer Manipulation](../vs140/Buffer-Manipulation.md)