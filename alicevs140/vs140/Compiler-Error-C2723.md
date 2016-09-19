---
title: "Compiler Error C2723"
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
ms.assetid: 86925601-2297-4cfd-94e2-2caf27c474c4
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C2723
'function' : 'specifier' specifier illegal on function definition  
  
 The specifier cannot appear with a function definition outside of a class declaration. The `virtual` specifier can be specified only on a member function declaration within a class declaration.  
  
 The following sample generates C2723 and shows how to fix it:  
  
```  
// C2723.cpp  
struct X {  
   virtual void f();  
   virtual void g();  
};  
  
virtual void X::f() {}   // C2723  
  
// try the following line instead  
void X::g() {}  
```