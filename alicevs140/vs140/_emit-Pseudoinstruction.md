---
title: "_emit Pseudoinstruction"
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
ms.assetid: 004c48f3-364c-4e82-9a51-e326f9cc7b2b
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _emit Pseudoinstruction
## Microsoft Specific  
 The **_emit** pseudoinstruction defines one byte at the current location in the current text segment. The **_emit** pseudoinstruction resembles the [DB](../vs140/DB.md) directive of MASM.  
  
 The following fragment places the bytes 0x4A, 0x43, and 0x4B into the code:  
  
```  
#define randasm __asm _emit 0x4A __asm _emit 0x43 __asm _emit 0x4B  
 .  
 .  
 .  
__asm {  
     randasm  
     }  
```  
  
> [!CAUTION]
>  If `_emit` generates instructions that modify registers, and you compile the application with optimizations, the compiler cannot determine what registers are affected. For example, if `_emit` generates an instruction that modifies the **rax** register, the compiler does not know that **rax** has changed. The compiler might then make an incorrect assumption about the value in that register after the inline assembler code executes. Consequently, your application might exhibit unpredictable behavior when it runs.  
  
 **END Microsoft Specific**  
  
## See Also  
 [Using Assembly Language in __asm Blocks](../vs140/Using-Assembly-Language-in-__asm-Blocks.md)