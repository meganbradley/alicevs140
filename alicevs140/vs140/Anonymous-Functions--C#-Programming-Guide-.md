---
title: "Anonymous Functions (C# Programming Guide)"
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
ms.assetid: 6ce3f04d-0c71-4728-9127-634c7e9a8365
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Anonymous Functions (C# Programming Guide)
An anonymous function is an "inline" statement or expression that can be used wherever a delegate type is expected. You can use it to initialize a named delegate or pass it instead of a named delegate type as a method parameter.  
  
 There are two kinds of anonymous functions, which are discussed individually in the following topics:  
  
-   [Lambda Expressions (C# Programming Guide)](../Topic/Lambda%20Expressions%20\(C%23%20Programming%20Guide\).md).  
  
-   [Anonymous Methods (C# Programming Guide)](../vs140/Anonymous-Methods--C#-Programming-Guide-.md)  
  
    > [!NOTE]
    >  Lambda expressions can be bound to expression trees and also to delegates.  
  
## The Evolution of Delegates in C#  
 In C# 1.0, you created an instance of a delegate by explicitly initializing it with a method that was defined elsewhere in the code. C# 2.0 introduced the concept of anonymous methods as a way to write unnamed inline statement blocks that can be executed in a delegate invocation. C# 3.0 introduced lambda expressions, which are similar in concept to anonymous methods but more expressive and concise. These two features are known collectively as *anonymous functions*. In general, applications that target version 3.5 and later of the [!INCLUDE[dnprdnshort](../vs140/includes/dnprdnshort_md.md)] should use lambda expressions.  
  
 The following example demonstrates the evolution of delegate creation from C# 1.0 to C# 3.0:  
  
 [!CODE [csProgGuideLINQ#65](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideLINQ#65)]  
  
## C# Language Specification  
 [!INCLUDE[CSharplangspec](../vs140/includes/Csharplangspec_md.md)]  
  
## See Also  
 [Statements, Expressions, and Operators (C# Programming Guide)](../vs140/Statements--Expressions--and-Operators--C#-Programming-Guide-.md)   
 [Lambda Expressions (C# Programming Guide)](../Topic/Lambda%20Expressions%20\(C%23%20Programming%20Guide\).md)   
 [Delegates (C# Programming Guide)](../Topic/Delegates%20\(C%23%20Programming%20Guide\).md)   
 [Expression Trees](../vs140/Expression-Trees--C#-and-Visual-Basic-.md)