---
title: "Compiler Error CS0674"
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
ms.assetid: 9ebfac30-6de8-4503-b4f0-d79f7398e3d5
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0674
Do not use 'System.ParamArrayAttribute'. Use the 'params' keyword instead.  
  
 The C# compiler does not allow for the use of <xref:System.ParamArrayAttribute?qualifyHint=True>; use [params](../vs140/params--C#-Reference-.md) instead.  
  
 The following sample generates CS0674:  
  
```  
// CS0674.cs  
using System;  
public class MyClass   
{  
  
   public static void UseParams([ParamArray] int[] list)   // CS0674  
   // try the following line instead  
   // public static void UseParams(params int[] list)   
   {  
      for ( int i = 0 ; i < list.Length ; i++ )  
         Console.WriteLine(list[i]);  
      Console.WriteLine();  
   }  
  
   public static void Main()   
   {  
      UseParams(1, 2, 3);  
   }  
}  
```