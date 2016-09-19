---
title: "Compiler Warning (level 4) C4710"
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
ms.topic: error-reference
ms.assetid: 76381ec7-3fc1-4bee-9a0a-c2c8307b92e2
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (level 4) C4710
'function' : function not inlined  
  
 The given function was selected for inline expansion, but the compiler did not perform the inlining.  
  
 Inlining is performed at the compiler's discretion. The **inline** keyword, like the **register** keyword, is used as a hint for the compiler. The compiler uses heuristics to determine if it should inline a particular function to speed up the code when compiling for speed, or if it should inline a particular function to make the code smaller when compiling for space. The compiler will only inline very small functions when compiling for space.  
  
 In some cases, the compiler will not inline a particular function for mechanical reasons. See [C4714](../vs140/Compiler-Warning--level-4--C4714.md) for a list of reasons the compiler may not inline a function.  
  
 This warning is off by default. See [Compiler Warnings That Are Off by Default](../vs140/Compiler-Warnings-That-Are-Off-by-Default.md) for more information.