---
title: "Compiler Error C2512"
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
ms.assetid: 15206da9-1164-451a-b869-280e00711aad
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C2512
'identifier' : no appropriate default constructor available  
  
 No default constructor is available for the specified class, structure, or union. The compiler supplies a default constructor only if user-defined constructors are not provided.  
  
 If you provide a constructor that takes a non-void parameter, and you want to allow your class to be created with no parameters—for example, as the elements of an array—you must also provide a default constructor. The default constructor can be a constructor with default values for all parameters.  
  
 The following sample generates C2512 and shows how to fix it:  
  
```  
// C2512.cpp  
// C2512 expected  
struct B {  
   B (char *);  
   // Uncomment the following line to fix.  
   // B() {};  
};  
  
int main() {  
   B b;   
}  
```  
  
 The following sample shows a more subtle C2512. To fix this error, rearrange the code to define the class before its constructor is referenced:  
  
```  
// C2512b.cpp  
// compile with: /c  
struct S {  
   struct X;  
  
   void f() {  
      X *x = new X();   // C2512 X not defined yet  
   }  
  
};  
  
struct S::X {};  
  
struct T {  
   struct X;  
   void f();  
};  
  
struct T::X {};  
  
void T::f() {  
   X *x = new X();  
}  
```  
  
 C2512 can also be caused by a call to default-construct a class that contains a const or reference data member. These members must be initialized in a constructor initializer list, which prevents the compiler from generating a default constructor.  
  
 The following sample generates C2512 and shows how to fix it:  
  
```  
// C2512c.cpp  
// Compile by using: cl /c /W3 C2512c.cpp  
struct S {  
   const int i_;  
   int &r_;   
};   
  
int SumS() {  
   const int ci = 7;  
   int ir = 42;  
  
   S s1; // C2512 - no default constructor available  
   S s2{ci, ir};  // Fix - initialize const and reference members   
   return s2.i_ + s2.r_;  
}  
```