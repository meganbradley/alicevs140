---
title: "Compiler Error C3653"
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
ms.assetid: 316549d7-f7ef-4578-a2ba-57adc8aac527
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C3653
'function' : cannot be used as a named override: a function being overridden not found; did you forget to name the function explicitly, using a :: operator?  
  
 An explicit override specified a function that was not found in any interface. For more information, see [Explicit Overrides](../vs140/Explicit-Overrides---C---Component-Extensions-.md).  
  
 The following sample generates C3653:  
  
```  
// C3653.cpp  
// compile with: /clr  
public interface struct I {  
   void h();  
};  
  
public ref struct X : public I {  
   virtual void f() new sealed = J {};   // C3653 no J in scope  
   virtual void g() {}   // OK  
   virtual void h() new sealed = I::h {};   // OK  
};  
```