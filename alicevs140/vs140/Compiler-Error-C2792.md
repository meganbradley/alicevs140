---
title: "Compiler Error C2792"
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
ms.assetid: 392cf748-4f5e-4e62-a364-3118d5658408
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C2792
'super' : this keyword must be followed by '::'  
  
 The only token that can follow the keyword `__super` is `::`.  
  
 The following sample generates C2792:  
  
```  
// C2792.cpp  
struct B {  
   void mf();  
};  
  
struct D : B {  
   void mf() {  
      __super.();   // C2792  
  
      // try the following line instead  
      // __super::mf();  
   }  
};  
```