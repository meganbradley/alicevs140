---
title: "Compiler Error C3670"
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
ms.assetid: d0fa9c6e-8f90-48c7-9066-31b4fa5942eb
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C3670
'override' : cannot override inaccessible base class method 'method'  
  
 An override can only take place on a function whose access level makes it available in a derived type. For more information, see [Explicit Overrides](../vs140/Explicit-Overrides---C---Component-Extensions-.md).  
  
 The following sample generates C3670:  
  
```  
// C3670.cpp  
// compile with: /clr /c  
public ref class C {  
// Uncomment the following line to resolve.  
// public:  
   virtual void g() { }  
};  
  
public ref class D : public C {  
public:  
   virtual void f() new sealed = C::g {};   // C3670  
};  
```