---
title: "_InterlockedAddLargeStatistic"
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
ms.assetid: 2802e74b-bcee-46e4-b562-894908d44409
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _InterlockedAddLargeStatistic
**Microsoft Specific**  
  
 Performs an interlocked addition in which the first operand is a 64-bit value.  
  
## Syntax  
  
```  
long _InterlockedAddLargeStatistic(  
   __int64 volatile * Addend,  
   long Value  
);  
```  
  
#### Parameters  
 [in, out] `Addend`  
 A pointer to the first operand to the add operation. The value pointed to is replaced by the result of the addition.  
  
 [in] `Value`  
 The second operand; value to add to the first operand.  
  
## Return Value  
 The value of the second operand.  
  
## Requirements  
  
|Intrinsic|Architecture|  
|---------------|------------------|  
|`_InterlockedAddLargeStatistic`|x86|  
  
 **Header file** <intrin.h>  
  
## Remarks  
 This intrinsic is not atomic because it is implemented as two separate locked instructions. An atomic 64-bit read that occurs on another thread during the execution of this intrinsic could result in an inconsistent value being read.  
  
 This function behaves as a read-write barrier. For more information, see [_ReadWriteBarrier](../vs140/_ReadWriteBarrier.md).  
  
## END Microsoft Specific  
  
## See Also  
 [Compiler Intrinsics](../vs140/Compiler-Intrinsics.md)   
 [Conflicts with the x86 Compiler](../vs140/Conflicts-with-the-x86-Compiler.md)