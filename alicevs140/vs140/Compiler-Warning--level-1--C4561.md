---
title: "Compiler Warning (level 1) C4561"
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
ms.assetid: 3a10c12c-601b-4b6c-9861-331fd022e021
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (level 1) C4561
'__fastcall' incompatible with the '/clr' option: converting to '\__stdcall'  
  
 The [__fastcall](../vs140/__fastcall.md) function-calling convention cannot be used with the [/clr](../Topic/-clr%20\(Common%20Language%20Runtime%20Compilation\).md) compiler option. The compiler ignores the calls to `__fastcall`. To fix this warning, either remove the calls to **__fastcall** or compile without **/clr**.  
  
 The following sample generates C4561:  
  
```  
// C4561.cpp  
// compile with: /clr /W1 /c  
// processor: x86  
void __fastcall Func(void *p);   // C4561, remove __fastcall to resolve  
```