---
title: "Compiler Error CS0241"
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
ms.assetid: be31b194-3de5-4aab-b23a-6cf790f940ab
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0241
Default parameter specifiers are not permitted  
  
 [Method parameters](../vs140/Method-Parameters--C#-Reference-.md) cannot have default values. Use method overloads if you want to achieve the same effect. For more information, see [Passing Parameters (C# Programmer's Reference)](../vs140/Passing-Parameters--C#-Programming-Guide-.md).  
  
## Example  
 The following sample generates CS0241. In addition, the sample shows how to simulate, with overloading, a method with default arguments.  
  
```  
// CS0241.cs  
public class A  
{  
   public void Test(int i = 9) {}   // CS0241  
}  
  
public class B  
{  
   public void Test() { Test(9); }  
   public void Test(int i)  {}  
}  
  
public class C  
{  
   public static void Main()  
   {   
      B x = new B();  
      x.Test();  
   }  
}  
```