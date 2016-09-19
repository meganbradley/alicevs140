---
title: "Compiler Error CS0193"
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
ms.assetid: 7b60fd99-9eee-4d61-ad75-585a16e22e96
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0193
The * or -> operator must be applied to a pointer  
  
 The **\*** or **->** operator was used with a nonpointer type. For more information, see [Pointer types (C# Programmers Reference)](../vs140/Pointer-types--C#-Programming-Guide-.md).  
  
 The following sample generates CS0193:  
  
```  
// CS0193.cs  
using System;  
  
public struct Age  
{  
   public int AgeYears;  
   public int AgeMonths;  
   public int AgeDays;  
}  
  
public class MyClass  
{  
   public static void SetAge(ref Age anAge, int years, int months, int days)  
   {  
      anAge->Months = 3;   // CS0193, anAge is not a pointer  
      // try the following line instead  
      // anAge.AgeMonths = 3;  
   }  
  
   public static void Main()  
   {  
      Age MyAge = new Age();  
      Console.WriteLine(MyAge.AgeMonths);  
      SetAge(ref MyAge, 22, 4, 15);  
      Console.WriteLine(MyAge.AgeMonths);  
   }  
}  
```