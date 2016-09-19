---
title: "Compiler Error C3240"
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
ms.assetid: 1a8dc213-b80c-47ae-ada0-e9554b635d1e
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C3240
'function' : must be a non-overloaded abstract member function of 'type'  
  
 A base type contained a function that was defined. Function must be virtual.  
  
## Example  
 The following sample generates C3240.  
  
```  
// C3240.cpp  
// compile with: /c  
__interface I {  
   void f();  
};  
  
struct A1 : I {   
   void f() {}  
};  
  
struct A2 : I {   
   void f() = 0;  
};  
  
template <class T>   
struct A3 : T {  
   void T::f() {}  
};  
  
template <class T>   
struct A4 : T {  
   void T::f() {}  
};  
  
A3<A1> x;   // C3240  
A3<I> x2;  
A4<A2> x3;  
```