---
title: "Compiler Warning (level 3) C4980"
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
ms.assetid: 2b7a0241-4791-4e29-a4bb-4e6baaeba0d2
caps.latest.revision: 17
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (level 3) C4980
'keyword' : use of this keyword requires /clr:oldSyntax command line option  
  
 A keyword from a previous version was used. Update your code to use newer syntax, or use [/clr:oldSyntax](../Topic/-clr%20\(Common%20Language%20Runtime%20Compilation\).md). For more information about the newer syntax, see [Language Features for Targeting the CLR](../Topic/Component%20Extensions%20for%20Runtime%20Platforms.md).  
  
 C4980 is a warning that is always issued as an error.  Use **/wd** to turn the warning off.  See [/w, /Wn, /WX, /Wall, /wln, /wdn, /wen, /won (Warning Level)](../Topic/-w,%20-W0,%20-W1,%20-W2,%20-W3,%20-W4,%20-w1,%20-w2,%20-w3,%20-w4,%20-Wall,%20-wd,%20-we,%20-wo,%20-Wv,%20-WX%20\(Warning%20Level\).md) for more information.  
  
 The following sample generates C4980:  
  
```  
// C4980.cpp  
// compile with: /clr  
int main() {  
   int x1 = 0;  
   int^ px = __box(x1);   // C4980  
   int^ px2 = x1;   // OK  
}  
```