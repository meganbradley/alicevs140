---
title: "Compiler Error CS1673"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - CSharp
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 5c7dd58b-dcbc-45c9-be36-7d15fafaa067
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS1673
Anonymous methods, lambda expressions, and query expressions inside structs cannot access instance members of 'this'. Consider copying 'this' to a local variable outside the anonymous method, lambda expression or query expression and using the local instead.  
  
 The following sample generates CS1673:  
  
```  
// CS1673.cs  
delegate int MyDelegate();  
  
public struct S  
{  
   int member;  
  
   public int F(int i)  
   {  
       member = i;  
       // Try assigning to a local variable  
       // S s = this;  
       MyDelegate d = delegate()  
       {  
          i = this.member;  // CS1673  
          // And use the local variable instead of "this"  
          // i =  s.member;  
          return i;  
  
       };  
       return d();  
   }  
}  
  
class CMain  
{  
   public static void Main()  
   {  
   }  
}  
```