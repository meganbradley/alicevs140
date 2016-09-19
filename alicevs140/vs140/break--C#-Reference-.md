---
title: "break (C# Reference)"
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
ms.assetid: be2571ed-efb0-4965-b122-81e5b09db0b9
caps.latest.revision: 23
translation.priority.ht: 
  - de-de
  - ja-jp
---
# break (C# Reference)
The `break` statement terminates the closest enclosing loop or [switch](../vs140/switch--C#-Reference-.md) statement in which it appears. Control is passed to the statement that follows the terminated statement, if any.  
  
## Example  
 In this example, the conditional statement contains a counter that is supposed to count from 1 to 100; however, the `break` statement terminates the loop after 4 counts.  
  
 [!CODE [csrefKeywordsJump#1](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsJump#1)]  
  
## Example  
 In this example, the `break` statement is used to break out of an inner nested loop, and return control to the outer loop.  
  
 [!CODE [csrefKeywordsJump#7](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsJump#7)]  
  
## Example  
 This example demonstrates the use of `break` in a [switch](../vs140/switch--C#-Reference-.md) statement.  
  
 [!CODE [csrefKeywordsJump#2](../CodeSnippet/VS_Snippets_VBCSharp/csrefKeywordsJump#2)]  
  
 If you entered `4`, the output would be:  
  
```  
Enter your selection (1, 2, or 3): 4  
Sorry, invalid selection.  
```  
  
## C# Language Specification  
 [!INCLUDE[CSharplangspec](../vs140/includes/Csharplangspec_md.md)]  
  
## See Also  
 [C# Reference](../vs140/C#-Reference.md)   
 [C# Programming Guide](../vs140/C#-Programming-Guide.md)   
 [C# Keywords](../Topic/C%23%20Keywords.md)   
 [switch](../vs140/switch--C#-Reference-.md)   
 [Jump Statements](../vs140/Jump-Statements--C#-Reference-.md)   
 [Iteration Statements (C# Reference)](../vs140/Iteration-Statements--C#-Reference-.md)