---
title: "Compiler Warning C4485"
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
ms.assetid: a6f2b437-ca93-4dcd-b9cb-df415e10df86
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning C4485
'override_function' : matches base ref class method 'base_class_function ', but is not marked 'new' or 'override'; 'new' (and 'virtual') is assumed  
  
 An accessor overrides, with or without the `virtual` keyword, a base class accessor function, but the `override` or `new` specifier was not part of the overriding function signature. Add the `new` or `override` specifier to resolve this warning.  
  
 See [override](../vs140/override---C---Component-Extensions-.md) and [new (new slot in vtable)](../vs140/new--new-slot-in-vtable----C---Component-Extensions-.md) for more information.  
  
 C4485 is always issued as an error. Use the [warning](../vs140/warning.md) pragma to suppress C4485.  
  
## Example  
 The following sample generates C4485  
  
```  
// C4485.cpp  
// compile with: /clr  
delegate void Del();  
  
ref struct A {  
   virtual event Del ^E;  
};  
  
ref struct B : A {  
   virtual event Del ^E;   // C4485  
};  
  
ref struct C : B {  
   virtual event Del ^E {  
      void raise() override {}  
      void add(Del ^) override {}  
      void remove(Del^) override {}  
   }  
};  
```