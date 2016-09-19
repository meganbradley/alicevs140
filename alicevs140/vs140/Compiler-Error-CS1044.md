---
title: "Compiler Error CS1044"
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
ms.assetid: 18fc1ff5-8b97-4c31-99a1-5985b8e58024
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS1044
Cannot use more than one type in a for, using, fixed, or declaration statement  
  
 The compiler found an invalid statement.  
  
 The following sample generates CS1044:  
  
```  
// CS1044.cs  
using System;  
  
public class MyClass : IDisposable  
{  
   public void Dispose()  
   {  
      Console.WriteLine("Res1.Dispose()");  
   }  
  
   public static void Main()  
   {  
      using (MyClass mc1 = new MyClass(),  
             MyClass mc2 = new MyClass())   // CS1044, remove an instantiation  
      {  
      }  
   }  
}  
```