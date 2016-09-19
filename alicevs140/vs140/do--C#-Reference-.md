---
title: "do (C# Reference)"
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
ms.assetid: 50725f79-9ba6-4898-aa78-6e331568a1bb
caps.latest.revision: 24
translation.priority.ht: 
  - de-de
  - ja-jp
---
# do (C# Reference)
The `do` statement executes a statement or a block of statements repeatedly until a specified expression evaluates to `false`. The body of the loop must be enclosed in braces, `{}`, unless it consists of a single statement. In that case, the braces are optional.  
  
## Example  
 In the following example, the `do-while` loop statements execute as long as the variable `x` is less than 5.  
  
 [!CODE [csrefKeywordsIteration#1](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsIteration#1)]  
  
 Unlike the [while](../vs140/while--C#-Reference-.md) statement, a `do-while` loop is executed one time before the conditional expression is evaluated.  
  
 At any point in the `do-while` block, you can break out of the loop using the [break](../vs140/break--C#-Reference-.md) statement. You can step directly to the `while` expression evaluation statement by using the [continue](../vs140/continue--C#-Reference-.md) statement. If the `while` expression evaluates to true, execution continues at the first statement in the loop. If the expression evaluates to false, execution continues at the first statement after the `do-while` loop.  
  
 A `do-while` loop can also be exited by the [goto](../vs140/goto--C#-Reference-.md), [return](../vs140/return--C#-Reference-.md), or [throw](../Topic/throw%20\(C%23%20Reference\).md) statements.  
  
## C# Language Specification  
 [!INCLUDE[CSharplangspec](../vs140/includes/Csharplangspec_md.md)]  
  
## See Also  
 [C# Reference](../vs140/C#-Reference.md)   
 [C# Programming Guide](../vs140/C#-Programming-Guide.md)   
 [C# Keywords](../Topic/C%23%20Keywords.md)   
 [do-while Statement (C++)](../vs140/do-while-Statement--C---.md)   
 [Iteration Statements](../vs140/Iteration-Statements--C#-Reference-.md)