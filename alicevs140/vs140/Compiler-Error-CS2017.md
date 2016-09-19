---
title: "Compiler Error CS2017"
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
ms.assetid: 16fd0c3b-018f-4734-809d-8d98d05a254c
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS2017
Cannot specify /main if building a module or library  
  
 You cannot specify a main entry point when you are building a [/target:library](../vs140/-target-library--C#-Compiler-Options-.md).  
  
 The following sample generates CS2017:  
  
```  
// CS2017.cs  
// compile with: /main:MyClass /target:library  
// CS2017 expected  
class MyClass  
{  
   public static void Main()  
   {  
   }  
}  
```