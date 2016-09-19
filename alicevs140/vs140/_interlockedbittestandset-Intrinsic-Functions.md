---
title: "_interlockedbittestandset Intrinsic Functions"
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
ms.assetid: b1b7e334-53ea-48cf-ba60-5fa3ef51a1fc
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _interlockedbittestandset Intrinsic Functions
**Microsoft Specific**  
  
 Generate an instruction which examines bit `b` of the address `a` and returns its current value before setting it to 1.  
  
## Syntax  
  
```  
unsigned char _interlockedbittestandset(  
   long *a,  
   long b  
);  
unsigned char _interlockedbittestandset_acq(  
   long *a,  
   long b  
);  
unsigned char _interlockedbittestandset_HLEAcquire(  
   long *a,  
   long b  
);  
unsigned char _interlockedbittestandset_HLERelease(  
   long *a,  
   long b  
);  
unsigned char _interlockedbittestandset_nf(  
   long *a,  
   long b  
);  
unsigned char _interlockedbittestandset_rel(  
   long *a,  
   long b  
);  
unsigned char _interlockedbittestandset64(  
   __int64 *a,  
   __int64 b  
);  
unsigned char _interlockedbittestandset64_HLEAcquire(  
   __int64 *a,  
   __int64 b  
);  
unsigned char _interlockedbittestandset64_HLERelease(  
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
 The value of the bit at position `b` before it is set.  
  
## Requirements  
  
|Intrinsic|Architecture|Header|  
|---------------|------------------|------------|  
|`_interlockedbittestandset`|x86, ARM, [!INCLUDE[vcprx64](../vs140/includes/vcprx64_md.md)]|<intrin.h>|  
|`_interlockedbittestandset_acq`, `_interlockedbittestandset_nf`, `_interlockedbittestandset_rel`|ARM|<intrin.h>|  
|`_interlockedbittestandset_HLEAcquire`, `_interlockedbittestandset_HLERelease`|x86, [!INCLUDE[vcprx64](../vs140/includes/vcprx64_md.md)]|<immintrin.h>|  
|`_interlockedbittestandset64`|[!INCLUDE[vcprx64](../vs140/includes/vcprx64_md.md)]|<intrin.h>|  
|`_interlockedbittestandset64_HLEAcquire`, `_interlockedbittestandset64_HLERelease`|[!INCLUDE[vcprx64](../vs140/includes/vcprx64_md.md)]|<immintrin.h>|  
  
## Remarks  
 On x86 and [!INCLUDE[vcprx64](../vs140/includes/vcprx64_md.md)] processors, these intrinsics use the `lock bts` instruction to read and set the specified bit to 1. The operation is atomic.  
  
 On ARM processors, use the intrinsics with `_acq` and `_rel` suffixes for acquire and release semantics, such as at the beginning and end of a critical section. The ARM intrinsics with an `_nf` ("no fence") suffix do not act as a memory barrier.  
  
 On Intel processors that support Hardware Lock Elision (HLE) instructions, the intrinsics with `_HLEAcquire` and `_HLERelease` suffixes include a hint to the processor that can accelerate performance by eliminating a lock write step in hardware. If these intrinsics are called on processors that do not support HLE, the hint is ignored.  
  
 These routines are only available as intrinsics.  
  
## END Microsoft Specific  
  
## See Also  
 [Compiler Intrinsics](../vs140/Compiler-Intrinsics.md)   
 [Conflicts with the x86 Compiler](../vs140/Conflicts-with-the-x86-Compiler.md)