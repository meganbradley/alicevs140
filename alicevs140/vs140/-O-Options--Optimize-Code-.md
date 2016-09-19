---
title: "-O Options (Optimize Code)"
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
H1: /O Options (Optimize Code)
ms.assetid: 77997af9-5555-4b3d-aa57-6615b27d4d5d
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# -O Options (Optimize Code)
The **/O** options control various optimizations that help you create code for maximum speed or minimum size.  
  
-   [/O1](../Topic/-O1,%20-O2%20\(Minimize%20Size,%20Maximize%20Speed\).md) optimizes code for minimum size.  
  
-   [/O2](../Topic/-O1,%20-O2%20\(Minimize%20Size,%20Maximize%20Speed\).md) optimizes code for maximum speed.  
  
-   [/Ob](../Topic/-Ob%20\(Inline%20Function%20Expansion\).md) controls inline function expansion.  
  
-   [/Od](../Topic/-Od%20\(Disable%20\(Debug\)\).md) disables optimization, speeding compilation and simplifying debugging.  
  
-   [/Og](../vs140/-Og--Global-Optimizations-.md) enables global optimizations.  
  
-   [/Oi](../vs140/-Oi--Generate-Intrinsic-Functions-.md) generates intrinsic functions for appropriate function calls.  
  
-   [/Os](../vs140/-Os---Ot--Favor-Small-Code--Favor-Fast-Code-.md) tells the compiler to favor optimizations for size over optimizations for speed.  
  
-   [/Ot](../vs140/-Os---Ot--Favor-Small-Code--Favor-Fast-Code-.md) (a default setting) tells the compiler to favor optimizations for speed over optimizations for size.  
  
-   [/Ox](../vs140/-Ox--Full-Optimization-.md) selects full optimization.  
  
-   [/Oy](../Topic/-Oy%20\(Frame-Pointer%20Omission\).md) suppresses the creation of frame pointers on the call stack for quicker function calls.  
  
## Remarks  
 You can also combine multiple **/O** options into a single option statement. For example, `/Odi` is the same as `/Od /Oi`.  
  
## See Also  
 [Compiler Options](../vs140/Compiler-Options.md)   
 [Setting Compiler Options](../vs140/Setting-Compiler-Options.md)