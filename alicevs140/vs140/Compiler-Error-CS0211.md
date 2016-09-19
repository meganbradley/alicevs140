---
title: "Compiler Error CS0211"
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
ms.assetid: 720be9a9-b0c1-4391-94e5-4c4027e83036
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0211
Cannot take the address of the given expression  
  
 You can take the address of fields, local variables, and indirection of pointers, but you cannot take, for example, the address of the sum of two local variables. For more information, see [Unsafe Code and Pointers (C# Programmers Reference)](../vs140/Unsafe-Code-and-Pointers--C#-Programming-Guide-.md).  
  
 The following sample generates CS0211:  
  
```  
// CS0211.cs  
// compile with: /unsafe  
  
public class MyClass  
{  
   unsafe public void M()  
   {  
      int a = 0, b = 0;  
      int *i = &(a + b);   // CS0211, the addition of two local variables  
      // try the following line instead  
      // int *i = &a;  
   }  
  
   public static void Main()  
   {  
   }  
}  
```