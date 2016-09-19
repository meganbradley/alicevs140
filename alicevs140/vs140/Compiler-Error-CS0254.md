---
title: "Compiler Error CS0254"
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
ms.assetid: 85b2ab1e-0011-4f1d-9181-76b9c9f3d914
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0254
The right hand side of a fixed statement assignment may not be a cast expression  
  
 The right side of a [fixed](../vs140/fixed-Statement--C#-Reference-.md) expression may not use a cast. For more information, see [Unsafe Code and Pointers (C# Programmer's Reference)](../vs140/Unsafe-Code-and-Pointers--C#-Programming-Guide-.md).  
  
 The following sample generates CS0254:  
  
```  
// CS0254.cs  
// compile with: /unsafe  
class Point  
{  
   public uint x, y;  
}  
  
class FixedTest  
{  
   unsafe static void SquarePtrParam (int* p)  
   {  
      *p *= *p;  
   }  
  
   unsafe public static void Main()  
   {  
      Point pt = new Point();  
      pt.x = 5;  
      pt.y = 6;  
  
      fixed (int* p = (int*)&pt.x)   // CS0254  
      // try the following line instead  
      // fixed (uint* p = &pt.x)  
      {  
         SquarePtrParam ((int*)p);  
      }  
   }  
}  
```