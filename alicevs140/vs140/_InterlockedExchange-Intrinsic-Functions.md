---
title: "_InterlockedExchange Intrinsic Functions"
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
ms.assetid: be2f232a-6301-462a-a92b-fcdeb8b0f209
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _InterlockedExchange Intrinsic Functions
**Microsoft Specific**  
  
 Generates an atomic instruction to set a specified value.  
  
## Syntax  
  
```  
long _InterlockedExchange(  
   long volatile * Target,  
   long Value  
);  
long _InterlockedExchange_acq(  
   long volatile * Target,  
   long Value  
);  
long _InterlockedExchange_HLEAcquire(  
   long volatile * Target,  
   long Value  
);  
long _InterlockedExchange_HLERelease(  
   long volatile * Target,  
   long Value  
);  
long _InterlockedExchange_nf(  
   long volatile * Target,  
   long Value  
);  
long _InterlockedExchange_rel(  
   long volatile * Target,  
   long Value  
);  
char _InterlockedExchange8(  
   char volatile * Target,  
   char Value  
);  
char _InterlockedExchange8_acq(  
   char volatile * Target,  
   char Value  
);  
char _InterlockedExchange8_nf(  
   char volatile * Target,  
   char Value  
);  
char _InterlockedExchange8_rel(  
   char volatile * Target,  
   char Value  
);  
short _InterlockedExchange16(  
   short volatile * Target,  
   short Value  
);  
short _InterlockedExchange16_acq(  
   short volatile * Target,  
   short Value  
);  
short _InterlockedExchange16_nf(  
   short volatile * Target,  
   short Value  
);  
short _InterlockedExchange16_rel(  
   short volatile * Target,  
   short Value  
);  
__int64 _InterlockedExchange64(  
   __int64 volatile * Target,  
   __int64 Value  
);  
__int64 _InterlockedExchange64_acq(  
   __int64 volatile * Target,  
   __int64 Value  
);  
__int64 _InterlockedExchange64_HLEAcquire(  
   __int64 volatile * Target,  
   __int64 Value  
);  
__int64 _InterlockedExchange64_HLERelease(  
   __int64 volatile * Target,  
   __int64 Value  
);  
__int64 _InterlockedExchange64_nf(  
   __int64 volatile * Target,  
   __int64 Value  
);  
__int64 _InterlockedExchange64_rel(  
   __int64 volatile * Target,  
   __int64 Value  
);  
```  
  
#### Parameters  
 [in, out] `Target`  
 Pointer to the value to be exchanged. The function sets this variable to `Value` and returns its prior value.  
  
 [in] `Value`  
 Value to be exchanged with the value pointed to by `Target`.  
  
## Return Value  
 Returns the initial value pointed to by `Target`.  
  
## Requirements  
  
|Intrinsic|Architecture|Header|  
|---------------|------------------|------------|  
|`_InterlockedExchange`, `_InterlockedExchange8`, `_InterlockedExchange16`, `_InterlockedExchange64`|x86, ARM, [!INCLUDE[vcprx64](../vs140/includes/vcprx64_md.md)]|<intrin.h>|  
|`_InterlockedExchange_acq`, `_InterlockedExchange_nf`, `_InterlockedExchange_rel`, `_InterlockedExchange8_acq`, `_InterlockedExchange8_nf`, `_InterlockedExchange8_rel`, `_InterlockedExchange16_acq`, `_InterlockedExchange16_nf`, `_InterlockedExchange16_rel`, `_InterlockedExchange64_acq`, `_InterlockedExchange64_nf`, `_InterlockedExchange64_rel`,|ARM|<intrin.h>|  
|`_InterlockedExchange_HLEAcquire`, `_InterlockedExchange_HLERelease`, `_InterlockedExchange64_HLEAcquire`, `_InterlockedExchange64_HLERelease`|x86, [!INCLUDE[vcprx64](../vs140/includes/vcprx64_md.md)]|<immintrin.h>|  
  
## Remarks  
 `_InterlockedExchange` provides compiler intrinsic support for the Win32 [!INCLUDE[winsdkshort](../vs140/includes/winsdkshort_md.md)] [InterlockedExchange](http://msdn.microsoft.com/library/ms683590.aspx) function.  
  
 There are several variations on `_InterlockedExchange` that vary based on the data types they involve and whether processor-specific acquire or release semantics is used.  
  
 While the `_InterlockedExchange` function operates on 32-bit integer values, `_InterlockedExchange8` operates on 8-bit integer values, `_InterlockedExchange16` operates on 16-bit integer values, and `_InterlockedExchange64` operates on 64-bit integer values.  
  
 On ARM platforms, use the intrinsics with `_acq` and `_rel` suffixes for acquire and release semantics, such as at the beginning and end of a critical section. The intrinsics with an `_nf` ("no fence") suffix do not act as a memory barrier.  
  
 On Intel platforms that support Hardware Lock Elision (HLE) instructions, the intrinsics with `_HLEAcquire` and `_HLERelease` suffixes include a hint to the processor that can accelerate performance by eliminating a lock write step in hardware. If these intrinsics are called on platforms that do not support HLE, the hint is ignored.  
  
 These routines are only available as intrinsics.  
  
## Example  
 For a sample of how to use `_InterlockedExchange`, see [_InterlockedDecrement](../vs140/_InterlockedDecrement-Intrinsic-Functions.md).  
  
## END Microsoft Specific  
  
## See Also  
 [Compiler Intrinsics](../vs140/Compiler-Intrinsics.md)   
 [Keywords](../vs140/Keywords--C---.md)   
 [Conflicts with the x86 Compiler](../vs140/Conflicts-with-the-x86-Compiler.md)