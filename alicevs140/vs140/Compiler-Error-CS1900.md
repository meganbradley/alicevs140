---
title: "Compiler Error CS1900"
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
ms.assetid: 08141138-bfea-4af3-a9a0-ec54cf2caa13
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS1900
Warning level must be in the range 0-4  
  
 The [/warn](../vs140/-warn--C#-Compiler-Options-.md) compiler option can only take one of five possible values (0, 1, 2, 3, or 4). Any other value passed to **/warn** will result in CS1900.  
  
 The following sample generates CS1900:  
  
```  
// CS1900.cs  
// compile with: /W:5  
// CS1900 expected  
class x  
{  
   public static void Main()  
   {  
   }  
}  
```