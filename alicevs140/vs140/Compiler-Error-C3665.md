---
title: "Compiler Error C3665"
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
ms.assetid: 893bb47e-8de1-43aa-af7d-fa47ad149ee9
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C3665
'destructor' : override specifier 'keyword' not allowed on a destructor/finalizer  
  
 A keyword was used that is not allowed on a destructor or finalizer.  
  
 For example, a new slot cannot be requested on a destructor or finalizer.  For more information, see [Explicit Overrides](../vs140/Explicit-Overrides---C---Component-Extensions-.md) and [Destructors and Finalizers](../Topic/How%20to:%20Define%20and%20Consume%20Classes%20and%20Structs%20\(C++-CLI\).md#BKMK_Destructors_and_finalizers).  
  
 The following sample generates C3665:  
  
```  
// C3665.cpp  
// compile with: /clr  
public ref struct R {  
   virtual ~R() { }  
   virtual void a() { }  
};  
  
public ref struct S : R {  
   virtual ~S() new {}   // C3665  
   virtual void a() new {}   // OK  
};  
```