---
title: "Compiler Error C3840"
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
ms.assetid: dfde76dd-a920-4228-9125-aa081a0de738
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C3840
declaration of 'method' not allowed; use destructors to implement finalization  
  
 Declare a destructor instead of a `Finalize` method in a managed class.  
  
 C3840 is only reachable using **/clr:oldSyntax**.  
  
 The following sample generates C3840:  
  
```  
// C3840.cpp  
// compile with: /clr:oldSyntax  
#using <mscorlib.dll>  
__gc class X  
{  
protected:  
  
   void Finalize()  
   {   // C3840, "declaration of 'X::Finalize' not allowed...  
   }  
  
   // declare a destructor instead  
   // ~X()  
   // {  
   // }  
};  
  
int main()  
{  
}  
```