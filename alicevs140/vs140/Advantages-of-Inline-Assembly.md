---
title: "Advantages of Inline Assembly"
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
ms.assetid: 94364d97-faa7-4bdf-8473-570956986c51
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Advantages of Inline Assembly
## Microsoft Specific  
 Because the inline assembler doesn't require separate assembly and link steps, it is more convenient than a separate assembler. Inline assembly code can use any C variable or function name that is in scope, so it is easy to integrate it with your program's C code. Because the assembly code can be mixed inline with C or C++ statements, it can do tasks that are cumbersome or impossible in C or C++.  
  
 The uses of inline assembly include:  
  
-   Writing functions in assembly language.  
  
-   Spot-optimizing speed-critical sections of code.  
  
-   Making direct hardware access for device drivers.  
  
-   Writing prolog and epilog code for "naked" calls.  
  
 Inline assembly is a special-purpose tool. If you plan to port an application to different machines, you'll probably want to place machine-specific code in a separate module. Because the inline assembler doesn't support all of Microsoft Macro Assembler's (MASM) macro and data directives, you may find it more convenient to use MASM for such modules.  
  
 **END Microsoft Specific**  
  
## See Also  
 [Inline Assembler](../vs140/Inline-Assembler.md)