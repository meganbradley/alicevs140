---
title: "Compiler Error C2790"
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
ms.assetid: 38d4fce1-ba00-413d-8bc1-e8aa43d7bc1f
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C2790
'super' : this keyword can only be used within the body of class member function  
  
 This error message appears if the user ever tries to uses the keyword [super](../vs140/__super.md) outside of the context of a member function.  
  
 The following sample generates C2790:  
  
```  
// C2790.cpp  
void f() {  
   __super::g();   // C2790  
}  
```