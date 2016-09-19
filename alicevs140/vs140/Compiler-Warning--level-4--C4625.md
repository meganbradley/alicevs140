---
title: "Compiler Warning (level 4) C4625"
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
ms.assetid: 4cc99e50-846c-4784-97da-48b977067851
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (level 4) C4625
'derived class' : copy constructor was implicitly defined as deleted because a base class copy constructor is inaccessible or deleted  
  
 A copy constructor was deleted or not accessible in a base class and was therefore not generated for a derived class. Any attempt to copy an object of this type will cause a compiler error.  
  
 This warning is off by default. See [Compiler Warnings That Are Off by Default](../vs140/Compiler-Warnings-That-Are-Off-by-Default.md) for more information.  
  
## Example  
 The following sample generates C4625 and shows how to fix it.  
  
```  
// C4625.cpp  
// compile with: /W4 /c  
#pragma warning(default : 4625)  
  
struct A {  
   A() {}  
  
private:  
   A(const A&) {}  
};  
  
struct C : private virtual A {};  
struct B :  C {};   // C4625 no copy constructor  
  
struct D : A {};  
struct E :  D {};   // OK  
```