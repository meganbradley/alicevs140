---
title: "Compiler Error C2027"
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
ms.assetid: a39150c0-ec04-45ec-934c-a838bfe76627
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C2027
use of undefined type 'type'  
  
 A type cannot be used until it is defined. To resolve the error, be sure the type is fully defined before referencing it.  
  
## Example  
 The following sample generates C2027.  
  
```  
// C2027.cpp  
class C;  
class D {  
public:  
   void func() {  
   }  
};  
  
int main() {  
   C *pC;  
   pC->func();   // C2027  
  
   D *pD;  
   pD->func();  
}  
```  
  
## Example  
 It is possible to declare a pointer to a declared but undefined type.  But Visual C++ does not allow a reference to an undefined type.  
  
 The following sample generates C2027.  
  
```  
// C2027_b.cpp  
class A;  
A& CreateA();  
  
class B;  
B* CreateB();  
  
int main() {  
   CreateA();   // C2027  
   CreateB();   // OK  
}  
```