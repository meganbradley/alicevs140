---
title: "Compiler Error CS0572"
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
ms.assetid: ec950e95-13da-41b5-90cd-9e673d62498b
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0572
'type' : cannot reference a type through an expression; try 'path_to_type' instead  
  
 An attempt was made to access a member of a class through an identifier, which is not permitted in this situation.  
  
 The following sample generates CS0572:  
  
```  
// CS0572.cs  
using System;  
class C  
{  
   public class Inner  
   {  
      public static int v = 9;  
   }  
}  
  
class D : C  
{  
   public static void Main()  
   {  
      C cValue = new C();  
      Console.WriteLine(cValue.Inner.v);   // CS0572  
      // try the following line instead  
      // Console.WriteLine(C.Inner.v);  
   }  
}  
```