---
title: "Linker Tools Error LNK1313"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: error-reference
ms.assetid: 5df0b72e-bb3f-428c-8d84-6084238f9827
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Linker Tools Error LNK1313
ijw/native module detected; cannot link with pure modules  
  
 The current version of Visual C++ does not support linking native or mixed managed/native .obj files with .obj files compiled with **/clr:pure**.  
  
## Example  
  
```  
// LNK1313.cpp  
// compile with: /c /clr:pure  
// a pure module  
int main() {}  
```  
  
## Example  
  
```  
// LNK1313_b.cpp  
// compile with: /c /clr  
// an IJW module  
void test(){}  
```  
  
## Example  
 The following sample will generate LNK1313.  
  
```  
// LNK1313_c.cpp  
// compile with: /link LNK1313.obj LNK1313_b.obj  
// LNK1313 warning expected  
```