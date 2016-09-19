---
title: "__faststorefence"
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
ms.assetid: 6c6eb973-3cf0-4306-b3af-cfde9b0210a5
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# __faststorefence
**Microsoft Specific**  
  
 Guarantees that every previous memory reference, including both load and store memory references, is globally visible before any subsequent memory reference.  
  
## Syntax  
  
```  
void __faststorefence();  
```  
  
## Requirements  
  
|Intrinsic|Architecture|  
|---------------|------------------|  
|`__faststorefence`|[!INCLUDE[vcprx64](../vs140/includes/vcprx64_md.md)]|  
  
 **Header file** <intrin.h>  
  
## Remarks  
 Generates a full memory barrier instruction sequence that guarantees load and store operations issued before this intrinsic are globally visible before execution continues. The effect is comparable to but faster than the `_mm_mfence` intrinsic on all x64 platforms.  
  
 On the AMD64 platform, this routine generates an instruction that is a faster store fence than the `sfence` instruction. For time-critical code, use this intrinsic instead of `_mm_sfence` only on AMD64 platforms. On Intel x64 platforms, the `_mm_sfence` instruction is faster.  
  
 This routine is only available as an intrinsic.  
  
## END Microsoft Specific  
  
## See Also  
 [Compiler Intrinsics](../vs140/Compiler-Intrinsics.md)