---
title: "Compiler Error CS1515"
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
ms.assetid: 17d9dbbe-14a0-4c80-a942-82fa6ec2b0b0
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS1515
'in' expected  
  
 In a [foreach, in](../Topic/foreach,%20in%20\(C%23%20Reference\).md) statement, the "in" part is missing.  
  
## Example  
 The following sample generates CS1515:  
  
```  
using System;  
  
class Driver  
{  
   static void Main()  
   {  
      int[] arr = new int[] {1, 2, 3};  
  
      // try the following line instead  
      // foreach (int x in arr)  
      foreach (int x arr)      // CS1515, "in" is missing  
      {  
         Console.WriteLine(x);  
      }  
   }  
}  
```