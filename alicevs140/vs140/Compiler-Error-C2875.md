---
title: "Compiler Error C2875"
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
ms.assetid: d589fc0c-08b2-4a79-bc0e-dca5eb80bdd5
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C2875
using-declaration causes a multiple declaration of 'class::identifier'  
  
 The declaration causes the same item to be defined twice.  
  
 The following sample generates C2875:  
  
```  
// C2875.cpp  
struct A {  
   void f(int*);  
};  
  
struct B {  
   void f(double*);  
};  
  
struct AB : A, B {  
   using A::f;  
   using A::f;   // C2875  
   using B::f;  
};  
```