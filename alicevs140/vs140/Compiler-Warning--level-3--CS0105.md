---
title: "Compiler Warning (level 3) CS0105"
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
ms.assetid: 96d1d5d7-79e9-424f-bbde-f87e88b70003
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (level 3) CS0105
The using directive for 'namespace' appeared previously in this namespace  
  
 A [namespace](../vs140/namespace--C#-Reference-.md), which should only be declared once, was declared more than once; remove all duplicate namespace declarations.  
  
 The following sample generates CS0105:  
  
```  
// CS0105.cs  
// compile with: /W:3  
using System;  
using System;   // CS0105  
  
public class a  
{  
   public static void Main()  
   {  
   }  
}  
```