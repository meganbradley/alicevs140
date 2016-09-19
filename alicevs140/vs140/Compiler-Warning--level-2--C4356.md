---
title: "Compiler Warning (level 2) C4356"
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
ms.assetid: 3af3defe-de33-43b6-bd6c-2c2e09e34f3f
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (level 2) C4356
'member' : static data member cannot be initialized via derived class  
  
 The initialization of a static data member was ill formed. The compiler accepted the initialization.  
  
 This is a breaking change in the Visual C++ .NET 2003 compiler.  
  
 For code that works the same in all versions of Visual C++, initialize the member through the base class.  
  
 Use the [warning](../vs140/warning.md) pragma to suppress this warning.  
  
 The following sample generates C4356:  
  
```  
// C4356.cpp  
// compile with: /W2 /EHsc  
#include <iostream>  
  
template <class T>  
class C {  
   static int n;  
};  
  
class D : C<int> {};  
  
int D::n = 0; // C4356  
// try the following line instead  
// int C<int>::n = 0;  
  
class A {  
public:  
   static int n;  
};  
  
class B : public A {};  
  
int B::n = 10;   // C4356  
// try the following line instead  
// int A::n = 99;  
  
int main() {  
   using namespace std;  
   cout << B::n << endl;  
}  
```