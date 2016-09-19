---
title: "Compiler Warning (level 4) C4487"
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
ms.assetid: 796144cf-cd3c-4edc-b6a4-96192b7eb4f0
caps.latest.revision: 6
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (level 4) C4487
'derived_class_function' : matches inherited non-virtual method 'base_class_function' but is not explicitly marked 'new'  
  
 A function in a derived class has the same signature as a non-virtual base class function. C4487 reminds you that the derived class function does not override the base class function. Explicitly mark the derived class function as `new` to resolve this warning.  
  
 For more information, see [new (new slot in vtable)](../vs140/new--new-slot-in-vtable----C---Component-Extensions-.md).  
  
## Example  
 The following sample generates C4487.  
  
```  
// C4487.cpp  
// compile with: /W4 /clr  
using namespace System;  
public ref struct B {  
   void f() { Console::WriteLine("in B::f"); }  
   void g() { Console::WriteLine("in B::g"); }  
};  
  
public ref struct D : B {  
   void f() { Console::WriteLine("in D::f"); }   // C4487  
   void g() new { Console::WriteLine("in D::g"); }   // OK  
};  
  
int main() {  
   B ^ a = gcnew D;  
   // will call base class functions  
   a->f();  
   a->g();  
}  
```