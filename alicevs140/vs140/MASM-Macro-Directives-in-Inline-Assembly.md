---
title: "MASM Macro Directives in Inline Assembly"
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
ms.assetid: 83643a09-1699-40a8-8ef2-13502bc4ac2c
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# MASM Macro Directives in Inline Assembly
## Microsoft Specific  
 The inline assembler is not a macro assembler. You cannot use MASM macro directives (**MACRO**, `REPT`, **IRC**, `IRP`, and `ENDM`) or macro operators (**<>**, **!**, **&**, `%`, and `.TYPE`). An `__asm` block can use C preprocessor directives, however. See [Using C or C++ in __asm Blocks](../vs140/Using-C-or-C---in-__asm-Blocks.md) for more information.  
  
 **END Microsoft Specific**  
  
## See Also  
 [Using Assembly Language in __asm Blocks](../vs140/Using-Assembly-Language-in-__asm-Blocks.md)