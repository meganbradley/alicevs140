---
title: "Compiler Error C2180"
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
ms.assetid: ea71b39e-b977-48a7-b7bd-af68ef5e263b
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C2180
controlling expression has type 'type'  
  
 The controlling expression in an `if`, `while`, `for`, or `do` statement is an expression cast to `void`. To fix this issue, change the controlling expression to one that produces a `bool` or a type that can be converted to `bool`.  
  
 The following sample generates C2180:  
  
```  
// C2180.c  
  
int main() {  
   while ((void)1)   // C2180  
      return 1;  
   while (1)         // OK  
      return 0;  
}  
```