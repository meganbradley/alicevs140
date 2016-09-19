---
title: "_InterlockedIncrement Intrinsic Functions"
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
ms.assetid: 37700615-f372-438b-bcef-d76e11839482
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _InterlockedIncrement Intrinsic Functions
**Microsoft Specific**  
  
 Provide compiler intrinsic support for the Win32 [!INCLUDE[winsdkshort](../vs140/includes/winsdkshort_md.md)] [InterlockedIncrement](http://msdn.microsoft.com/library/ms683614.aspx) function.  
  
## Syntax  
  
```  
long _InterlockedIncrement(  
   long * lpAddend  
);  
long _InterlockedIncrement_acq(  
   long * lpAddend  
);  
long _InterlockedIncrement_rel(  
   long * lpAddend  
);  
long _InterlockedIncrement_nf(  
   long * lpAddend  
);  
short _InterlockedIncrement16(  
   short * lpAddend  
);  
short _InterlockedIncrement16_acq(  
   short * lpAddend  
);  
short _InterlockedIncrement16_rel(  
   short * lpAddend  
);  
short _InterlockedIncrement16_nf (  
   short * lpAddend  
);  
__int64 _InterlockedIncrement64(  
   __int64 * lpAddend  
);  
__int64 _InterlockedIncrement64_acq(  
   __int64 * lpAddend  
);  
__int64 _InterlockedIncrement64_rel(  
   __int64 * lpAddend  
);   
__int64 _InterlockedIncrement64_nf(  
   __int64 * lpAddend  
);  
```  
  
#### Parameters  
 [in, out] `lpAddend`  
 Pointer to the variable to be incremented.  
  
## Return Value  
 The return value is the resulting incremented value.  
  
## Requirements  
  
|Intrinsic|Architecture|Header|  
|---------------|------------------|------------|  
|`_InterlockedIncrement`, `_InterlockedIncrement16`, `_InterlockedIncrement64`|x86, ARM, [!INCLUDE[vcprx64](../vs140/includes/vcprx64_md.md)]|<intrin.h>|  
|`_InterlockedIncrement_acq`, `_InterlockedIncrement_rel`, `_InterlockedIncrement_nf`, `_InterlockedIncrement16_acq`, `_InterlockedIncrement16_rel`, `_InterlockedIncrement16_nf`, `_InterlockedIncrement64_acq`, `_InterlockedIncrement64_rel`, `_InterlockedIncrement64_nf`|ARM|<intrin.h>|  
  
## Remarks  
 There are several variations on `_InterlockedIncrement` that vary based on the data types they involve and whether processor-specific acquire or release semantics is used.  
  
 While the `_InterlockedIncrement` function operates on 32-bit integer values, `_InterlockedIncrement16` operates on 16-bit integer values and `_InterlockedIncrement64` operates on 64-bit integer values.  
  
 On ARM platforms, use the intrinsics with `_acq` and `_rel` suffixes if you need acquire and release semantics, such as at the beginning and end of a critical section. The intrinsic with an `_nf` ("no fence") suffix does not act as a memory barrier.  
  
 The variable pointed to by the `lpAddend` parameter must be aligned on a 32-bit boundary; otherwise, this function fails on multiprocessor x86 systems and any non-x86 systems. For more information, see [align](../vs140/align--C---.md).  
  
 The Win32 function is declared in `Wdm.h` or `Ntddk.h`.  
  
 These routines are only available as intrinsics.  
  
## Example  
 For a sample of how to use `_InterlockedIncrement`, see [_InterlockedDecrement](../vs140/_InterlockedDecrement-Intrinsic-Functions.md).  
  
## END Microsoft Specific  
  
## See Also  
 [Compiler Intrinsics](../vs140/Compiler-Intrinsics.md)   
 [Keywords](../vs140/Keywords--C---.md)   
 [Conflicts with the x86 Compiler](../vs140/Conflicts-with-the-x86-Compiler.md)