---
title: "Compiler Error C3257"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 511c2f9f-dfdd-4662-8436-e44fcd2bb5b9
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C3257
'object' : explicit call to ctor of __gc class type not allowed (did you forget 'new'?)  
  
 You cannot create temporary stack-based objects for managed classes. The compiler attempted to create a temporary object that is not directly mentioned in the code. This temporary object is created on the stack because there is no call to [new](../vs140/new-Operator--C---.md).  
  
 C3257 is only reachable using **/clr:oldSyntax**.  
  
 The following sample generates C3257:  
  
```  
// C3257a.cpp  
// compile with: /clr:oldSyntax /c  
__gc class X {  
public:  
   X();  
   X(int i) {  
      X();   // C3257  
      X *MyX = new X();   // OK  
   }  
};  
```