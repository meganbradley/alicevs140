---
title: "Compiler Error C3811"
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
ms.assetid: fbb98c21-f8d0-4910-91fa-570508c8f658
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C3811
property methods 'get_accessor' and 'set_accessor' must agree on their 'static' specifier  
  
 Event accessors must agree on their use of `static`.  
  
 C3811 is only reachable using **/clr:oldSyntax**.  
  
 The following sample generates C3811:  
  
```  
// C3811.cpp  
// compile with: /clr:oldSyntax  
#using <mscorlib.dll>  
  
__gc class X  
{  
   __property static int get_Size()  
   {  
      return 0;  
   }  
  
   __property void set_Size()  
   {   // C3811, add static to set_Size or remove from get_Size  
   }  
};  
  
int main()  
{  
}  
```