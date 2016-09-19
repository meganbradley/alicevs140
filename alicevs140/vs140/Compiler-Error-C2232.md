---
title: "Compiler Error C2232"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 76f302b7-30a7-4a81-9a39-b4edde33b54c
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C2232
'–>' : left operand has 'class-key' type, use '.'  
  
 The operand to the left of the `->` operator is not a pointer. Use the period (.) operator for a class, structure, or union.  
  
 The following sample generates C2232:  
  
```  
// C2232.c  
struct X {  
    int member;  
} x, *px;  
int main() {  
    x->member = 0;   // C2232, x is not a pointer  
  
    px->member = 0;  
    x.member = 0;  
}  
```