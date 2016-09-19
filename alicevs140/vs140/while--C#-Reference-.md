---
title: "while (C# Reference)"
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
ms.assetid: 72a0765c-6852-4aca-b327-4a11cb7f5c59
caps.latest.revision: 24
translation.priority.ht: 
  - de-de
  - ja-jp
---
# while (C# Reference)
The `while` statement executes a statement or a block of statements until a specified expression evaluates to `false`.  
  
## Example  
 [!CODE [csrefKeywordsIteration#5](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsIteration#5)]  
  
## Example  
 [!CODE [csrefKeywordsIteration#6](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsIteration#6)]  
  
## Example  
 Because the test of the `while` expression takes place before each execution of the loop, a `while` loop executes zero or more times. This differs from the [do](../vs140/do--C#-Reference-.md) loop, which executes one or more times.  
  
 A `while` loop can be terminated when a [break](../vs140/break--C#-Reference-.md), [goto](../vs140/goto--C#-Reference-.md), [return](../vs140/return--C#-Reference-.md), or [throw](../Topic/throw%20\(C%23%20Reference\).md) statement transfers control outside the loop. To pass control to the next iteration without exiting the loop, use the [continue](../vs140/continue--C#-Reference-.md) statement. Notice the difference in output in the three previous examples, depending on where `int n` is incremented. In the example below no output is generated.  
  
 [!CODE [csrefKeywordsIteration#7](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsIteration#7)]  
  
## C# Language Specification  
 [!INCLUDE[CSharplangspec](../vs140/includes/Csharplangspec_md.md)]  
  
## See Also  
 [C# Reference](../vs140/C#-Reference.md)   
 [C# Programming Guide](../vs140/C#-Programming-Guide.md)   
 [C# Keywords](../Topic/C%23%20Keywords.md)   
 [while Statement (C++)](../vs140/while-Statement--C---.md)   
 [Iteration Statements](../vs140/Iteration-Statements--C#-Reference-.md)