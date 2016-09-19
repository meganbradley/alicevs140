---
title: "Compiler Error CS0220"
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
ms.assetid: f520bf34-bff8-4796-882b-1a9b1d5b977c
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0220
The operation overflows at compile time in checked mode  
  
 An operation was detected by [checked](../vs140/checked--C#-Reference-.md), which is the default, and a data loss resulted. Either correct the inputs to the assignment or use [unchecked](../vs140/unchecked--C#-Reference-.md) to resolve this error. For more information, see [Checked and Unchecked (C# Programmers Reference)](../vs140/Checked-and-Unchecked--C#-Reference-.md).  
  
 The following sample generates CS0220:  
  
```  
// CS0220.cs  
using System;  
  
class TestClass  
{  
   const int x = 1000000;  
   const int y = 1000000;  
  
   public int MethodCh()  
   {  
      int z = (x * y);   // CS0220  
      return z;  
   }  
  
   public int MethodUnCh()  
   {  
      unchecked  
      {  
         int z = (x * y);  
         return z;  
      }  
   }  
  
   public static void Main()  
   {  
      TestClass myObject = new TestClass();  
      Console.WriteLine("Checked  : {0}", myObject.MethodCh());  
      Console.WriteLine("Unchecked: {0}", myObject.MethodUnCh());  
   }  
}  
```