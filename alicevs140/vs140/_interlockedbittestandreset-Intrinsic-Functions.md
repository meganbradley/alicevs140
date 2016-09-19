---
title: "_interlockedbittestandreset Intrinsic Functions"
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
ms.assetid: 9bbb1442-f2e9-4dc2-b0da-97f3de3493b9
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _interlockedbittestandreset Intrinsic Functions
**Microsoft Specific**  
  
 Generates an instruction which sets bit `b` of the address `a` to zero and returns its original value.  
  
## Syntax  
  
```  
unsigned char _interlockedbittestandreset(  
   long *a,  
   long b  
);  
unsigned char _interlockedbittestandreset_acq(  
   long *a,  
   long b  
);  
unsigned char _interlockedbittestandreset_HLEAcquire(  
   long *a,  
   long b  
);  
unsigned char _interlockedbittestandreset_HLERelease(  
   long *a,  
   long b  
);  
unsigned char _interlockedbittestandreset_nf(  
   long *a,  
   long b  
);  
unsigned char _interlockedbittestandreset_rel(  
   long *a,  
   long b  
);   
unsigned char _interlockedbittestandreset64(  
   __int64 *a,  
   __int64 b  
);   
unsigned char _interlockedbittestandreset64_HLEAcquire(  
   __int64 *a,  
   __int64 b  
);  
unsigned char _interlockedbittestandreset64_HLERelease(  
   __int64 *a,  
   __int64 b  
);  
```  
  
#### Parameters  
 [in] `a`  
 A pointer to the memory to examine.  
  
 [in] `b`  
 The bit position to test.  
  
## Return Value  
 The original value of the bit at the position specified by `b`.  
  
## Requirements  
  
|Intrinsic|Architecture|Header|  
|---------------|------------------|------------|  
|`_interlockedbittestandreset`|x86, ARM, [!INCLUDE[vcprx64](../vs140/includes/vcprx64_md.md)]|<intrin.h>|  
|`_interlockedbittestandreset_acq`, `_interlockedbittestandreset_nf`, `_interlockedbittestandreset_rel`|ARM|<intrin.h>|  
|`_interlockedbittestandreset_HLEAcquire`, `_interlockedbittestandreset_HLERelease`|x86, [!INCLUDE[vcprx64](../vs140/includes/vcprx64_md.md)]|<immintrin.h>|  
|`_interlockedbittestandreset64`|[!INCLUDE[vcprx64](../vs140/includes/vcprx64_md.md)]|<intrin.h>|  
|`_interlockedbittestandreset64_HLEAcquire`, `_interlockedbittestandreset64_HLERelease`|[!INCLUDE[vcprx64](../vs140/includes/vcprx64_md.md)]|<immintrin.h>|  
  
## Remarks  
 On x86 and [!INCLUDE[vcprx64](../vs140/includes/vcprx64_md.md)] processors, these intrinsics use the `lock btr` instruction, that reads and sets the specified bit to zero in an atomic operation.  
  
 On ARM processors, use the intrinsics with `_acq` and `_rel` suffixes for acquire and release semantics, such as at the beginning and end of a critical section. The ARM intrinsics with an `_nf` ("no fence") suffix do not act as a memory barrier.  
  
 On Intel processors that support Hardware Lock Elision (HLE) instructions, the intrinsics with `_HLEAcquire` and `_HLERelease` suffixes include a hint to the processor that can accelerate performance by eliminating a lock write step in hardware. If these intrinsics are called on processors that do not support HLE, the hint is ignored.  
  
 These routines are only available as intrinsics.  
  
## END Microsoft Specific  
  
## See Also  
 [Compiler Intrinsics](../vs140/Compiler-Intrinsics.md)   
 [Conflicts with the x86 Compiler](../vs140/Conflicts-with-the-x86-Compiler.md)