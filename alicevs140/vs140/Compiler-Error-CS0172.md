---
title: "Compiler Error CS0172"
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
ms.assetid: 1272c575-3580-4897-95fb-83f45d7435ae
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0172
Type of conditional expression cannot be determined because 'type1' and 'type2' implicitly convert to one another  
  
 In a conditional statement, you must be able to convert the types on either side of the `:` operator. Also, there cannot be mutual conversion routines; you only need one conversion. For more information, see [Conversion Operators (C# Programmers Reference)](../Topic/Conversion%20Operators%20\(C%23%20Programming%20Guide\).md).  
  
 The following sample generates CS0172:  
  
```  
// CS0172.cs  
public class Square  
{  
   public class Circle  
   {  
      public static implicit operator Circle(Square aa)  
      {  
         return null;  
      }  
  
      public static implicit operator Square(Circle aa)  
      // using explicit resolves this error  
      // public static explicit operator Square(Circle aa)  
      {  
         return null;  
      }  
   }  
  
   public static void Main()  
   {  
      Circle aa = new Circle();  
      Square ii = new Square();  
      object o = (1 == 1) ? aa : ii;   // CS0172  
      // the following cast would resolve this error  
      // (1 == 1) ? aa : (Circle)ii;  
   }  
}  
```