---
title: "Compiler Error CS1528"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - CSharp
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 38aabc5c-b32f-4bea-a585-c4212f42751d
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS1528
Expected ; or = (cannot specify constructor arguments in declaration)  
  
 A reference to a class was formed as if an object to the class was being created. For example, there was an attempt to pass a variable to a constructor. Use the [new](../vs140/new--C#-Reference-.md) operator to create an object of a class.  
  
 The following sample generates CS1528:  
  
```  
// CS1528.cs  
using System;  
  
public class B  
{  
   public B(int i)  
   {  
      _i = i;  
   }  
  
   public void PrintB()  
   {  
      Console.WriteLine(_i);  
   }  
  
   private int _i;  
}  
  
public class mine  
{  
   public static void Main()  
   {  
      B b(3);   // CS1528, reference is not an object  
      // try one of the following  
      // B b;  
      // or  
      // B bb = new B(3);  
      // bb.PrintB();  
   }  
}  
```