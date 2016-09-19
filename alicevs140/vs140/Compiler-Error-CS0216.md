---
title: "Compiler Error CS0216"
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
ms.assetid: afb3dd29-3eff-4b62-8267-eb726c2bcee4
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0216
The operator 'operator' requires a matching operator 'missing_operator' to also be defined  
  
 A user-defined [true](../vs140/true--C#-Reference-.md) operator requires a user-defined [false](../vs140/false--C#-Reference-.md) operator, and vice versa. For more information, see [Operators (C# Programmers Reference)](../Topic/Operators%20\(C%23%20Programming%20Guide\).md).  
  
 The following sample generates CS0216:  
  
```  
// CS0216.cs  
class MyClass  
{  
   public static bool operator true (MyClass MyInt)   // CS0216  
   {  
      return true;  
   }  
  
   // to resolve, uncomment the following operator definition  
   /*  
   public static bool operator false (MyClass MyInt)  
   {  
      return true;  
   }  
   */  
  
   public static void Main()  
   {  
   }  
}  
```