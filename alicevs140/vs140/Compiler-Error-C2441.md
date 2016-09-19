---
title: "Compiler Error C2441"
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
ms.assetid: ffbd6573-777a-48dd-892f-5cf4a758dcab
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C2441
'variable' : a symbol declared with __declspec(process) must be const in /clr:pure mode  
  
 By default, variables are per application domain under **/clr:pure**. A variable marked `__declspec(process)` under **/clr:pure** is prone to errors if modified in one application domain and read in another.  
  
 Therefore, the compiler enforces per process variables be `const` under **/clr:pure**, making them read only in all application domains.  
  
 For more information, see [process](../vs140/process.md) and [/clr (Common Language Runtime Compilation)](../Topic/-clr%20\(Common%20Language%20Runtime%20Compilation\).md).  
  
## Example  
 The following sample generates C2441.  
  
```  
// C2441.cpp  
// compile with: /clr:pure /c  
__declspec(process) int i;   // C2441  
__declspec(process) const int j = 0;   // OK  
```