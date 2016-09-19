---
title: "Compiler Error C2760"
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
ms.assetid: 585757fd-d519-43f3-94e5-50316ac8b90b
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C2760
syntax error : expected 'name1' not 'name2'  
  
 A casting operator is used with an invalid operator.  
  
 The following sample generates C2760:  
  
```  
// C2760.cpp  
class B {};  
class D : public B {};  
  
void f(B* pb) {  
    D* pd1 = static_cast<D*>(pb);  
    D* pd2 = static_cast<D*>=(pb);  // C2760  
    D* pd3 = static_cast<D*=(pb);   // C2760  
}  
```