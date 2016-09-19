---
title: "Compiler Error CS0149"
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
ms.assetid: c3c0e48e-8dba-4ee6-86fd-cbb02c68255c
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0149
Method name expected  
  
 When creating a [delegate](../vs140/delegate--C#-Reference-.md), specify a method. For more information, see [Delegates (C# Programmer's Reference)](../Topic/Delegates%20\(C%23%20Programming%20Guide\).md).  
  
 The following sample generates CS0149:  
  
```  
// CS0149.cs  
using System;  
  
delegate string MyDelegate(int i);  
  
class MyClass  
{  
   // class member-field of the declared delegate type  
   static MyDelegate dt;     
  
   public static void Main()  
   {  
      dt = new MyDelegate(17.45);   // CS0149  
      // try the following line instead  
      // dt = new MyDelegate(Func2);  
      F(dt);  
   }  
  
   public static string Func2(int j)  
   {  
      Console.WriteLine(j);  
      return j.ToString();  
   }  
  
   public static void F(MyDelegate myFunc)  
   {  
      myFunc(8);  
   }  
}  
```