---
title: "Compiler Error C3633"
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
ms.assetid: 7d65babf-2191-4d67-a69f-f5c4c2ddf946
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C3633
cannot define 'member' as a member of managed 'type'  
  
 CLR reference class data members cannot be of a non-POD C++ type.  You can only instantiate a POD native type in a CLR type.  For example, a POD type cannot contain a copy constructor or an assignment operator.  
  
## Example  
 The following sample generates C3633.  
  
```  
// C3633.cpp  
// compile with: /clr /c  
#pragma warning( disable : 4368 )  
  
class A1 {  
public:  
   A1() { II = 0; }  
   int II;  
};  
  
ref class B {  
public:  
   A1 a1;   // C3633  
   A1 * a2;   // OK  
   B() : a2( new A1 ) {}  
    ~B() { delete a2; }  
};  
```  
  
## Example  
 The following sample generates C3633.  
  
```  
// C3633_b.cpp  
// compile with: /clr:oldSyntax /c  
class A1 {  
public:  
   A1() { II = 0; }  
   int II;  
};  
  
__gc class B {  
public:  
   A1 a1;   // C3633  
   A1 * a2;   // OK  
   B() : a2( new A1 ) {}  
    ~B() { delete a2; }  
};  
```