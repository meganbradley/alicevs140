---
title: "Compiler Error CS1585"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - CSharp
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 429268c3-2dae-4c71-9e0d-be1badb3ca68
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS1585
Member modifier 'keyword' must precede the member type and name  
  
 The access specifier in a method signature did not occur in the correct location.  
  
 The following sample generates CS1585:  
  
```  
// CS1585.cs  
public class Class1  
{  
   public void static Main(string[] args)   // CS1585  
   // try the following line instead  
   // public static void Main(string[] args)  
   {  
   }  
}  
```