---
title: "Compiler Error C2571"
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
ms.assetid: c6522616-dee9-4d7d-9bf8-30a7e1deaadf
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C2571
'function' : virtual function cannot be in union 'union'  
  
 A union is declared with a virtual function. You can declare a virtual function only in a class or structure.  Possible resolutions:  
  
1.  Change the union to a class or structure.  
  
2.  Make the function nonvirtual.  
  
 The following sample generates C2571:  
  
```  
// C2571.cpp  
// compile with: /c  
union A {  
   virtual void func1();   // C2571  
   void func2();   // OK  
};  
```