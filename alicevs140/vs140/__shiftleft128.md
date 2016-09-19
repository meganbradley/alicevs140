---
title: "__shiftleft128"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 557b846a-8fb0-469d-91ac-1b1fad80dc2a
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# __shiftleft128
**Microsoft Specific**  
  
 Shifts a 128-bit quantity, represented as two 64-bit quantities `LowPart` and `HighPart`, to the left by a number of bits specified by `Shift` and returns the high 64 bits of the result.  
  
## Syntax  
  
```  
unsigned __int64 __shiftleft128(   
   unsigned __int64 LowPart,   
   unsigned __int64 HighPart,   
   unsigned char Shift   
);  
```  
  
#### Parameters  
 [in] `LowPart`  
 The low 64 bits of the 128-bit quantity to shift.  
  
 [in] `HighPart`  
 The high 64 bits of the 128-bit quantity to shift.  
  
 [in] `Shift`  
 The number of bits to shift.  
  
## Return Value  
 The high 64 bits of the result.  
  
## Requirements  
  
|Intrinsic|Architecture|  
|---------------|------------------|  
|`__shiftleft128`|[!INCLUDE[vcprx64](../vs140/includes/vcprx64_md.md)]|  
  
 **Header file** <intrin.h>  
  
## Remarks  
 The `Shift` value is always modulo 64 so that, for example, if you call `__shiftleft128(1, 0, 64)`, the function will shift the low part `0` bits left and return a high part of `0` and not `1` as might otherwise be expected.  
  
## Example  
  
```  
// shiftleft128.c  
// processor: IPF, x64  
#include <stdio.h>  
#include <intrin.h>  
  
#pragma intrinsic (__shiftleft128, __shiftright128)  
  
int main()  
{  
    unsigned __int64 i = 0x1I64;  
    unsigned __int64 j = 0x10I64;  
    unsigned __int64 ResultLowPart;  
    unsigned __int64 ResultHighPart;  
  
    ResultLowPart = i << 1;  
    ResultHighPart = __shiftleft128(i, j, 1);  
  
    // concatenate the low and high parts padded with 0's  
    // to display correct hexadecimal 128 bit values  
    printf_s("0x%02I64x%016I64x << 1 = 0x%02I64x%016I64x\n",  
             j, i, ResultHighPart, ResultLowPart);  
  
    ResultHighPart = j >> 1;  
    ResultLowPart = __shiftright128(i, j, 1);  
  
    printf_s("0x%02I64x%016I64x >> 1 = 0x%02I64x%016I64x\n",  
             j, i, ResultHighPart, ResultLowPart);    
}  
```  
  
 **0x100000000000000001 << 1 = 0x200000000000000002**  
**0x100000000000000001 >> 1 = 0x080000000000000000**   
## END Microsoft Specific  
  
## See Also  
 [__shiftright128](../vs140/__shiftright128.md)   
 [Compiler Intrinsics](../vs140/Compiler-Intrinsics.md)