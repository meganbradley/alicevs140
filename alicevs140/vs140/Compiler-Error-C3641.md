---
title: "Compiler Error C3641"
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
ms.assetid: e8d3613e-5e8d-46fe-a516-eb7d1de7cd21
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C3641
'function' : invalid calling convention 'calling_convention' for function compiled with /clr:pure or /clr:safe  
  
 Only [__clrcall](../Topic/__clrcall.md) calling convention is allowed with [/clr:pure](../Topic/-clr%20\(Common%20Language%20Runtime%20Compilation\).md).  
  
 The following sample generates C3641:  
  
```  
// C3641.cpp  
// compile with: /clr:pure /c  
void __cdecl f() {}   // C3641  
```