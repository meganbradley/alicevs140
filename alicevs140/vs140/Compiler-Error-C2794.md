---
title: "Compiler Error C2794"
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
ms.assetid: d508191c-9044-4c6a-9119-4bca668c0b93
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C2794
'function' : is not a member of any direct or indirect base class of 'class'  
  
 You tried to use [super](../vs140/__super.md) to call a nonexistent member function.  
  
 The following sample generates C2794  
  
```  
// C2794.cpp  
struct B {  
   void mf();  
};  
  
struct D : B {  
   void mf() {  
      __super::f();  // C2794  
   }  
};  
```