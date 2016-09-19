---
title: "Compiler Error C3631"
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
ms.assetid: 88cbd2d5-6fef-4940-be34-d8cbe816d3da
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C3631
'function': cannot overload managed or WinRT events  
  
 A managed or WinRT event cannot be overloaded.  
  
## Example  
 C3631 is only reachable using **/clr:oldSyntax**.  
  
 The following sample generates C3631.  
  
```  
// C3631.cpp  
// compile with: /clr:oldSyntax /c  
  
public __gc struct S2 {  
   __event void func1();     
   __event void func1(int);   // C3631 delete second declaration of func1  
};  
  
public __gc struct S1 {  
   __delegate void del1();  
   __delegate void del2();  
   __event int add_myE(del1*) { return 0; }     
   __event int remove_myE(del1*) { return 0; }     
   __event int add_myE(del2*) { return 0; }   // C3631  
   __event int remove_myE(del2*) { return 0; }   // C3631  
};  
```