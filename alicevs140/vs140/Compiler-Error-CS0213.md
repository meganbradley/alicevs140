---
title: "Compiler Error CS0213"
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
ms.assetid: 3c1d55e3-2b84-4c28-8206-ef65869a898c
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0213
You cannot use the fixed statement to take the address of an already fixed expression  
  
 A local variable in an [unsafe](../vs140/unsafe--C#-Reference-.md) method or a parameter is already fixed (on the stack), so you cannot take the address of either of these two variables in a [fixed](../vs140/fixed-Statement--C#-Reference-.md) expression. For more information, see [Unsafe Code and Pointers (C# Programmer's Reference)](../vs140/Unsafe-Code-and-Pointers--C#-Programming-Guide-.md).  
  
## Example  
 The following sample generates CS0213.  
  
```  
// CS0213.cs  
// compile with: /unsafe  
public class MyClass  
{  
   unsafe public static void Main()  
   {  
      int i = 45;  
      fixed (int *j = &i) { }  // CS0213  
      // try the following line instead  
      // int* j = &i;  
  
      int[] a = new int[] {1,2,3};  
      fixed (int *b = a)  
      {  
         fixed (int *c = b) { }  // CS0213  
         // try the following line instead  
         // int *c = b;  
      }  
   }  
}  
```