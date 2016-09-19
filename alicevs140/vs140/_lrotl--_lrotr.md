---
title: "_lrotl, _lrotr"
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
  - _lrotl
  - _lrotr
apilocation: 
  - msvcr100.dll
  - msvcr120.dll
  - msvcr90.dll
  - msvcr110_clr0400.dll
  - msvcr110.dll
  - msvcr80.dll
  - msvcrt.dll
apitype: DLLExport
ms.assetid: d42f295b-35f9-49d2-9ee4-c66896ffe68e
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _lrotl, _lrotr
Rotates bits to the left (`_lrotl`) or right (`_lrotr`).  
  
## Syntax  
  
```  
  
      unsigned long _lrotl(  
   unsigned long value,  
   int shift   
);  
unsigned long _lrotr(  
   unsigned long value,  
   int shift   
);  
```  
  
#### Parameters  
 *value*  
 Value to be rotated.  
  
 `shift`  
 Number of bits to shift *value*.  
  
## Return Value  
 Both functions return the rotated value. There is no error return.  
  
## Remarks  
 The `_lrotl` and `_lrotr` functions rotate *value* by `shift` bits. `_lrotl` rotates the value left. `_lrotr` rotates the value right. Both functions wrap bits rotated off one end of *value* to the other end.  
  
## Requirements  
  
|Routine|Required header|  
|-------------|---------------------|  
|`_lrotl`|<stdlib.h>|  
|`_lrotr`|<stdlib.h>|  
  
 For more compatibility information, see [Compatibility](../vs140/Compatibility.md) in the Introduction.  
  
## Libraries  
 All versions of the [C run-time libraries](../vs140/CRT-Library-Features.md).  
  
## Example  
  
```  
// crt_lrot.c  
  
#include <stdlib.h>  
#include <stdio.h>  
  
int main( void )  
{  
   unsigned long val = 0x0fac35791;  
  
   printf( "0x%8.8lx rotated left eight times is 0x%8.8lx\n",   
            val, _lrotl( val, 8 ) );  
   printf( "0x%8.8lx rotated right four times is 0x%8.8lx\n",   
            val, _lrotr( val, 4 ) );  
}  
```  
  
## Output  
  
```  
0xfac35791 rotated left eight times is 0xc35791fa  
0xfac35791 rotated right four times is 0x1fac3579  
```  
  
## .NET Framework Equivalent  
 Not applicable. To call the standard C function, use `PInvoke`. For more information, see [Platform Invoke Examples](assetId:///15926806-f0b7-487e-93a6-4e9367ec689f).  
  
## See Also  
 [Floating-Point Support](../vs140/Floating-Point-Support.md)   
 [_rotl, _rotl64, _rotr, _rotr64](../vs140/_rotl--_rotl64--_rotr--_rotr64.md)