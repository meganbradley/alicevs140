---
title: "Compiler Warning C4484"
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
ms.assetid: 3d30e5b3-2297-45b7-a37a-1360056fdd0e
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning C4484
'override_function' : matches base ref class method 'base_class_function', but is not marked 'virtual', 'new' or 'override'; 'new' (and not 'virtual') is assumed  
  
 When compiling with **/clr**, the compiler will not implicitly override a base class function, which means the function will get a new slot in the vtable. To resolve, explicitly specify whether a function is an override.  
  
 For more information, see:  
  
-   [/clr (Common Language Runtime Compilation)](../Topic/-clr%20\(Common%20Language%20Runtime%20Compilation\).md)  
  
-   [override](../vs140/override---C---Component-Extensions-.md)  
  
-   [new (new slot in vtable)](../vs140/new--new-slot-in-vtable----C---Component-Extensions-.md)  
  
 C4484 is always issued as an error. Use the [warning](../vs140/warning.md) pragma to suppress C4484.  
  
## Example  
 The following sample generates C4484.  
  
```  
// C4484.cpp  
// compile with: /clr  
ref struct A {  
   virtual void Test() {}  
};  
  
ref struct B : A {  
   void Test() {}   // C4484  
};  
  
// OK  
ref struct C {  
   virtual void Test() {}  
   virtual void Test2() {}  
};  
  
ref struct D : C {  
   virtual void Test() new {}  
   virtual void Test2() override {}  
};  
```