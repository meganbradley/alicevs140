---
title: "__shiftright128"
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
ms.assetid: 5419a6c4-0de1-43fb-b314-4faa5b2d051f
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# __shiftright128
**Microsoft Specific**  
  
 Shifts a 128-bit quantity, represented as two 64-bit quantities `LowPart` and `HighPart`, to the right by a number of bits specified by `Shift` and returns the low 64 bits of the result.  
  
## Syntax  
  
```  
unsigned __int64 __shiftright128(   
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
 The low 64 bits of the result.  
  
## Requirements  
  
|Intrinsic|Architecture|  
|---------------|------------------|  
|`__shiftright128`|[!INCLUDE[vcprx64](../vs140/includes/vcprx64_md.md)]|  
  
 **Header file** <intrin.h>  
  
## Remarks  
 The `Shift` value is always modulo 64 so that, for example, if you call `__shiftright128(0, 1, 64)`, the function will shift the high part `0` bits right and return a low part of `0` and not `1` as might otherwise be expected.  
  
## Example  
 For an example, see [__shiftleft128](../vs140/__shiftleft128.md).  
  
## END Microsoft Specific  
  
## See Also  
 [__shiftleft128](../vs140/__shiftleft128.md)   
 [Compiler Intrinsics](../vs140/Compiler-Intrinsics.md)