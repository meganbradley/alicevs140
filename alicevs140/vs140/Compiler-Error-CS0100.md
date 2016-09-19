---
title: "Compiler Error CS0100"
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
ms.assetid: b49e4846-2a82-48ed-9ca8-953eb5c1baaa
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0100
The parameter name 'parameter name' is a duplicate  
  
 A method declaration used the same parameter name more than once. Parameter names must be unique in a method declaration. For more information, see [Class and Struct Methods (C# Programmer's Reference)](../Topic/Methods%20\(C%23%20Programming%20Guide\).md).  
  
 The following sample generates CS0100:  
  
```  
// CS0100.cs  
namespace x  
{  
   public class a  
   {  
      public static void f(int i, char i)   // CS0100  
      // try the following line instead  
      // public static void f(int i, char j)  
      {  
      }  
  
      public static void Main()  
      {  
      }  
   }  
}  
```