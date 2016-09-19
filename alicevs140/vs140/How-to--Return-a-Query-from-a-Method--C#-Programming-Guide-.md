---
title: "How to: Return a Query from a Method (C# Programming Guide)"
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
ms.assetid: 9d6f20a7-f085-44cf-9df3-71948255ec68
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Return a Query from a Method (C# Programming Guide)
This example shows how to return a query from a method as the return value and as an `out` parameter.  
  
 Any query must have a type of <xref:System.Collections.IEnumerable?qualifyHint=False> or <xref:System.Collections.Generic.IEnumerable`1?qualifyHint=False>, or a derived type such as <xref:System.Linq.IQueryable`1?qualifyHint=False>. Therefore any return value or `out` parameter of a method that returns a query must also have that type. If a method materializes a query into a concrete <xref:System.Collections.Generic.List`1?qualifyHint=False> or <xref:System.Array?qualifyHint=False> type, it is considered to be returning the query results instead of the query itself. A query variable that is returned from a method can still be composed or modified.  
  
## Example  
 In the following example, the first method returns a query as a return value, and the second method returns a query as an `out` parameter. Note that in both cases it is a query that is  returned, not query results.  
  
 [!CODE [csProgGuideLINQ#80](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideLINQ#80)]  
  
## Compiling the Code  
  
-   Create a [!INCLUDE[vs_current_short](../vs140/includes/vs_current_short_md.md)] project that targets the .NET Framework version 3.5 or a later version. By default, the project has a reference to System.Core.dll and a `using` directive for the System.Linq namespace.  
  
-   Replace the class with the code in the example.  
  
-   Press F5 to compile and run the program.  
  
-   Press any key to exit the console window.  
  
## See Also  
 [LINQ Query Expressions (C# Programming Guide)](../Topic/LINQ%20Query%20Expressions%20\(C%23%20Programming%20Guide\).md)