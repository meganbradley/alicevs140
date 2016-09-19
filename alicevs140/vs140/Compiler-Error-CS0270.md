---
title: "Compiler Error CS0270"
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
ms.topic: error-reference
ms.assetid: ce3eaf5f-5c49-4608-a172-d92c515cab50
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0270
Array size cannot be specified in a variable declaration (try initializing with a 'new' expression)  
  
 This error occurs when a size is specified as part of an array declaration. To resolve, use the [new Operator](../vs140/new-Operator--C#-Reference-.md) expression.  
  
 The following example generates CS0270:  
  
```  
// CS0270.cs  
// compile with: /t:module  
  
public class Test  
{  
   int[10] a;   // CS0270  
   // To resolve, use the following line instead:  
   // int[] a = new int[10];  
}  
```