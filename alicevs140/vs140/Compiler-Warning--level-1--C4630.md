---
title: "Compiler Warning (level 1) C4630"
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
ms.assetid: d8926376-7acc-4fc7-8438-6f0de3468870
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (level 1) C4630
'symbol' : 'extern' storage class specifier illegal on member definition  
  
 A data member or member function is defined as `extern`. Members cannot be external, although entire objects can. The compiler ignores the `extern` keyword. The following sample generates C4630:  
  
```  
// C4630.cpp  
// compile with: /W1 /LD  
class A {  
   void func();  
};  
  
extern void A::func() {   // C4630, remove 'extern' to resolve  
}  
```