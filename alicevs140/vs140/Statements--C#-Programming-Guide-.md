---
title: "Statements (C# Programming Guide)"
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
ms.assetid: 901bcde7-87de-4e15-833c-f9cfd40c8ce3
caps.latest.revision: 30
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Statements (C# Programming Guide)
The actions that a program takes are expressed in statements. Common actions include declaring variables, assigning values, calling methods, looping through collections, and branching to one or another block of code, depending on a given condition. The order in which statements are executed in a program is called the flow of control or flow of execution. The flow of control may vary every time that a program is run, depending on how the program reacts to input that it receives at run time.  
  
 A statement can consist of a single line of code that ends in a semicolon, or a series of single-line statements in a block. A statement block is enclosed in {} brackets and can contain nested blocks. The following code shows two examples of single-line statements, and a multi-line statement block:  
  
 [!CODE [csProgGuideStatements#1](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideStatements#1)]  
  
## Types of Statements  
 The following table lists the various types of statements in C# and their associated keywords, with links to topics that include more information:  
  
|Category|C# keywords / notes|  
|--------------|---------------------------|  
|Declaration statements|A declaration statement introduces a new variable or constant. A variable declaration can optionally assign a value to the variable. In a constant declaration, the assignment is required.<br /><br /> [!CODE [csProgGuideStatements#23](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideStatements#23)]|  
|Expression statements|Expression statements that calculate a value must store the value in a variable.<br /><br /> [!CODE [csProgGuideStatements#24](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideStatements#24)]|  
|[Selection statements](../vs140/Selection-Statements--C#-Reference-.md)|Selection statements enable you to branch to different sections of code, depending on one or more specified conditions. For more information, see the following topics:<br /><br /> [if](../vs140/if-else--C#-Reference-.md), [else](../vs140/if-else--C#-Reference-.md), [switch](../vs140/switch--C#-Reference-.md), [case](../vs140/switch--C#-Reference-.md)|  
|[Iteration statements](../vs140/Iteration-Statements--C#-Reference-.md)|Iteration statements enable you to loop through collections like arrays, or perform the same set of statements repeatedly until a specified condition is met. For more information, see the following topics:<br /><br /> [do](../vs140/do--C#-Reference-.md), [for](../vs140/for--C#-Reference-.md), [foreach](../Topic/foreach,%20in%20\(C%23%20Reference\).md), [in](../Topic/foreach,%20in%20\(C%23%20Reference\).md), [while](../vs140/while--C#-Reference-.md)|  
|[Jump statements](../vs140/Jump-Statements--C#-Reference-.md)|Jump statements transfer control to another section of code. For more information, see the following topics:<br /><br /> [break](../vs140/break--C#-Reference-.md), [continue](../vs140/continue--C#-Reference-.md), [default](../vs140/switch--C#-Reference-.md), [goto](../vs140/goto--C#-Reference-.md), [return](../vs140/return--C#-Reference-.md), [yield](../Topic/yield%20\(C%23%20Reference\).md)|  
|[Exception handling statements](../vs140/Exception-Handling-Statements--C#-Reference-.md)|Exception handling statements enable you to gracefully recover from exceptional conditions that occur at run time. For more information, see the following topics:<br /><br /> [throw](../Topic/throw%20\(C%23%20Reference\).md), [try-catch](../Topic/try-catch%20\(C%23%20Reference\).md), [try-finally](../vs140/try-finally--C#-Reference-.md), [try-catch-finally](../vs140/try-catch-finally--C#-Reference-.md)|  
|[Checked and unchecked](../vs140/Checked-and-Unchecked--C#-Reference-.md)|Checked and unchecked statements enable you to specify whether numerical operations are allowed to cause an overflow when the result is stored in a variable that is too small to hold the resulting value. For more information, see [checked](../vs140/checked--C#-Reference-.md) and [unchecked](../vs140/unchecked--C#-Reference-.md).|  
he `await` statement|If you mark a method with the [async](../Topic/async%20\(C%23%20Reference\).md) modifier, you can use the [await](../Topic/await%20\(C%23%20Reference\).md) operator in the method. When control reaches an `await` expression in the async method, control returns to the caller, and progress in the method is suspended until the awaited task completes. When the task is complete, execution can resume in the method.<br /><br /> For a simple example, see the "Async Methods" section of [Methods (C# Programming Guide)](../Topic/Methods%20\(C%23%20Programming%20Guide\).md). For more information, see [Asynchronous Programming with Async and Await (C# and Visual Basic)](../vs140/Asynchronous-Programming-with-Async-and-Await--C#-and-Visual-Basic-.md).|  
|The `yield return` statement|An iterator performs a custom iteration over a collection, such as a list or an array. An iterator uses the [yield return](../Topic/yield%20\(C%23%20Reference\).md) statement to return each element one at a time. When a `yield return` statement is reached, the current location in code is remembered. Execution is restarted from that location when the iterator is called the next time.<br /><br /> For more information, see [Iterators (C# and Visual Basic)](../vs140/Iterators--C#-and-Visual-Basic-.md).|  
|The `fixed` statement|The fixed statement prevents the garbage collector from relocating a movable variable. For more information, see [fixed](../vs140/fixed-Statement--C#-Reference-.md).|  
|The `lock` statement|The lock statement enables you to limit access to blocks of code to only one thread at a time. For more information, see [lock](../Topic/lock%20Statement%20\(C%23%20Reference\).md).|  
|Labeled statements|You can give a statement a label and then use the [goto](../vs140/goto--C#-Reference-.md) keyword to jump to the labeled statement. (See the example in the following row.)|  
|The empty statement|The empty statement consists of a single semicolon. It does nothing and can be used in places where a statement is required but no action needs to be performed. The following examples show two uses for an empty statement:<br /><br /> [!CODE [csProgGuideStatements#25](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideStatements#25)]|  
  
## Embedded Statements  
 Some statements, including [do](../vs140/do--C#-Reference-.md), [while](../vs140/while--C#-Reference-.md), [for](../vs140/for--C#-Reference-.md), and [foreach](../Topic/foreach,%20in%20\(C%23%20Reference\).md), always have an embedded statement that follows them. This embedded statement may be either a single statement or multiple statements enclosed by {} brackets in a statement block. Even single-line embedded statements can be enclosed in {} brackets, as shown in the following example:  
  
 [!CODE [csProgGuideStatements#26](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideStatements#26)]  
  
 An embedded statement that is not enclosed in {} brackets cannot be a declaration statement or a labeled statement. This is shown in the following example:  
  
 [!CODE [csProgGuideStatements#27](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideStatements#27)]  
  
 Put the embedded statement in a block to fix the error:  
  
 [!CODE [csProgGuideStatements#28](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideStatements#28)]  
  
## Nested Statement Blocks  
 Statement blocks can be nested, as shown in the following code:  
  
 [!CODE [csProgGuideStatements#29](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideStatements#29)]  
  
## Unreachable Statements  
 If the compiler determines that the flow of control can never reach a particular statement under any circumstances, it will produce warning CS0162, as shown in the following example:  
  
 [!CODE [csProgGuideStatements#22](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideStatements#22)]  
  
## Related Sections  
  
-   [Statement Keywords (C# Reference)](../vs140/Statement-Keywords--C#-Reference-.md)  
  
-   [Expressions (Visual C#)](../Topic/Expressions%20\(C%23%20Programming%20Guide\).md)  
  
-   [Operators (Visual C#)](../Topic/Operators%20\(C%23%20Programming%20Guide\).md)  
  
## C# Language Specification  
 [!INCLUDE[CSharplangspec](../vs140/includes/Csharplangspec_md.md)]  
  
## See Also  
 [C# Programming Guide](../vs140/C#-Programming-Guide.md)