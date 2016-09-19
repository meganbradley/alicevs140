---
title: "Compiler Error C3421"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: b52050c6-17a4-424a-8894-337b0cec7010
caps.latest.revision: 5
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C3421
'type' : you cannot call the finalizer for this class as it is either inaccessible or it does not exist  
  
 A finalizer is implicitly private, so it cannot be called from outside its enclosing type.  
  
 For more information, see [Destructors and Finalizers](../vs140/Destructors-and-Finalizers-in-Visual-C--.md).  
  
## Example  
 The following sample generates C3421.  
  
```  
// C3421.cpp  
// compile with: /clr  
ref class A {};  
  
ref class B {   
   !B() {}  
  
public:  
   ~B() {}  
};  
  
int main() {  
   A a;  
   a.!A();   // C3421  
  
   B b;  
   b.!B();   // C3421  
}  
```