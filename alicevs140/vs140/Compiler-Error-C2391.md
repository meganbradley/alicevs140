---
title: "Compiler Error C2391"
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
ms.assetid: 63a9c6b9-03cc-4517-885c-bdcd048643b3
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C2391
'identifier' : 'friend' cannot be used during type definition  
  
 The `friend` declaration includes a complete class declaration. A `friend` declaration can specify a member function or an elaborated type specifier, but not a complete class declaration.  
  
 The following sample generates C2326:  
  
```  
// C2391.cpp  
// compile with: /c  
class D {   
   void func( int );   
};  
  
class A {  
   friend class B { int i; };   // C2391  
  
   // OK  
   friend class C;  
   friend void D::func(int);  
};  
```