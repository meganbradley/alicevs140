---
title: "Compiler Error C3671"
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
ms.assetid: d684e4ae-87e2-4424-80bb-6f346652c831
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C3671
'function_1' : function does not override 'function_2'  
  
 When using explicit override syntax, the compiler generates an error if a function is not overridden.  See [Explicit Overrides](../vs140/Explicit-Overrides---C---Component-Extensions-.md) for more information.  
  
## Example  
 The following sample generates C3671.  
  
```  
// C3671.cpp  
// compile with: /clr /c  
ref struct S {  
   virtual void f();  
};  
  
ref struct S1 : S {  
   virtual void f(int) new sealed = S::f;   // C3671  
   virtual void f() new sealed = S::f;  
};  
```