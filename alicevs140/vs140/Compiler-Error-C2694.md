---
title: "Compiler Error C2694"
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
ms.assetid: 8dc2cec2-67ae-4e16-8c0c-374425aca8bc
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C2694
'override': overriding virtual function has less restrictive exception specification than base class virtual member function 'base'  
  
 A virtual function was overridden, but under [/Za](../Topic/-Za,%20-Ze%20\(Disable%20Language%20Extensions\).md), the overriding function had a less restrictive [exception specification](../vs140/Exception-Specifications--throw---C---.md).  
  
 The following sample generates C2694:  
  
```  
// C2694.cpp  
// compile with: /Za /c  
class MyBase {  
public:  
   virtual void f(void) throw(int) {  
   }  
};  
  
class Derived : public MyBase {  
public:  
   void f(void) throw(...) {}   // C2694  
   void f2(void) throw(int) {}   // OK  
};  
```