---
title: "Compiler Error C3267"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: fc8807b4-1861-43cd-96a5-94f4fbfa90cb
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C3267
'class' : a class-constructor must be fully defined within the enclosing class  
  
 Class constructors must be fully defined within the enclosing class definition.  
  
 C3267 is only reachable using **/clr:oldSyntax**.  
  
 The following sample generates C3267:  
  
```  
// C3267.cpp  
// compile with: /clr:oldSyntax  
#using <mscorlib.dll>  
  
__gc class X {  
   public:  
   static X(); // C3267  
  
   /* use the lines below to resolve the error  
   static X() {  
   }     
   */  
};  
  
int main() {  
}  
```