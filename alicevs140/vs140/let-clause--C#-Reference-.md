---
title: "let clause (C# Reference)"
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
ms.assetid: 13c9c1a4-ce57-48ef-8e1b-4c2a59b99fb4
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# let clause (C# Reference)
In a query expression, it is sometimes useful to store the result of a sub-expression in order to use it in subsequent clauses. You can do this with the `let` keyword, which creates a new range variable and initializes it with the result of the expression you supply. Once initialized with a value, the range variable cannot be used to store another value. However, if the range variable holds a queryable type, it can be queried.  
  
## Example  
 In the following example `let` is used in two ways:  
  
1.  To create an enumerable type that can itself be queried.  
  
2.  To enable the query to call `ToLower` only one time on the range variable `word`. Without using `let`, you would have to call `ToLower` in each predicate in the `where` clause.  
  
 [!CODE [cscsrefQueryKeywords#28](../CodeSnippet/VS_Snippets_VBCSharp/CsCsrefQueryKeywords#28)]  
  
## See Also  
 [C# Reference](../vs140/C#-Reference.md)   
 [Query Keywords (C# Reference)](../vs140/Query-Keywords--C#-Reference-.md)   
 [LINQ Query Expressions (C# Programming Guide)](../Topic/LINQ%20Query%20Expressions%20\(C%23%20Programming%20Guide\).md)   
 [Getting Started with LINQ in C#](../vs140/Getting-Started-with-LINQ-in-C#.md)   
 [How To: Avoid Exceptions in Query Expressions](../vs140/How-to--Handle-Exceptions-in-Query-Expressions--C#-Programming-Guide-.md)