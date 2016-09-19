---
title: "Passing Parameters (C# Programming Guide)"
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
ms.assetid: a5c3003f-7441-4710-b8b1-c79de77e0b77
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Passing Parameters (C# Programming Guide)
In C#, arguments can be passed to parameters either by value or by reference. Passing by reference enables function members, methods, properties, indexers, operators, and constructors to change the value of the parameters and have that change persist in the calling environment. To pass a parameter by reference, use the `ref` or `out` keyword. For simplicity, only the `ref` keyword is used in the examples in this topic. For more information about the difference between `ref` and `out`, see [ref](../vs140/ref--C#-Reference-.md), [out](../vs140/out--C#-Reference-.md), and [Passing Arrays Using ref and out](../vs140/Passing-Arrays-Using-ref-and-out--C#-Programming-Guide-.md).  
  
 The following example illustrates the difference between value and reference parameters.  
  
 [!CODE [csProgGuideParameters#10](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideParameters#10)]  
  
 For more information, see the following topics:  
  
-   [Passing Value-Type Parameters](../vs140/Passing-Value-Type-Parameters--C#-Programming-Guide-.md)  
  
-   [Passing Reference-Type Parameters](../vs140/Passing-Reference-Type-Parameters--C#-Programming-Guide-.md)  
  
## C# Language Specification  
 [!INCLUDE[CSharplangspec](../vs140/includes/Csharplangspec_md.md)]  
  
## See Also  
 [C# Programming](../vs140/C#-Programming-Guide.md)   
 [Methods (C# Programming Guide)](../Topic/Methods%20\(C%23%20Programming%20Guide\).md)