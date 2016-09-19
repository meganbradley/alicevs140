---
title: "Compiler Error C2798"
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
ms.assetid: fb0cd861-b228-4f81-8090-e28344a727e0
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C2798
'super::member' is ambiguous  
  
 Multiple inherited structures contain the member you referenced with [super](../vs140/__super.md). You could fix the error by either:  
  
-   Removing B1 or B2 from the inheritance list of D.  
  
-   Changing the name of the data member in B1 or B2.  
  
 The following sample generates C2798:  
  
```  
// C2798.cpp  
struct B1 {  
   int i;  
};  
  
struct B2 {  
   int i;  
};  
  
struct D : B1, B2 {  
   void g() {  
      __super::i = 4; // C2798  
   }  
};  
```