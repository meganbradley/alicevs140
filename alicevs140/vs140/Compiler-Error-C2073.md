---
title: "Compiler Error C2073"
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
ms.assetid: 57908234-be7a-4ce9-b0a7-8b1ad621865e
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C2073
'identifier' : elements of partially initialized array must have a default constructor  
  
 Too few initializers were specified for an array of user-defined types or constants. If an explicit initializer and its corresponding constructor are not specified for an array member, a default constructor must be supplied.  
  
 The following sample generates C2073:  
  
```  
// C2073.cpp  
class A {  
public:  
   A( int );   // constructor for ints only  
};  
A a[3] = { A(1), A(2) };   // C2073, no default constructor  
```  
  
```  
// C2073b.cpp  
// compile with: /c  
class B {  
public:  
   B();   // default constructor declared  
   B( int );  
};  
B b[3] = { B(1), B(2) };   // OK  
```