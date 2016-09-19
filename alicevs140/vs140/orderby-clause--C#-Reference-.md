---
title: "orderby clause (C# Reference)"
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
ms.assetid: 21f87f48-d69d-4e95-9a52-6fec47b37e1f
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# orderby clause (C# Reference)
In a query expression, the `orderby` clause causes the returned sequence or subsequence (group) to be sorted in either ascending or descending order. Multiple keys can be specified in order to perform one or more secondary sort operations. The sorting is performed by the default comparer for the type of the element. The default sort order is ascending. You can also specify a custom comparer. However, it is only available by using method-based syntax. For more information, see [Sorting Data](../vs140/Sorting-Data.md).  
  
## Example  
 In the following example, the first query sorts the words in alphabetical order starting from A, and second query sorts the same words in descending order. (The `ascending` keyword is the default sort value and can be omitted.)  
  
 [!CODE [cscsrefQueryKeywords#20](../CodeSnippet/VS_Snippets_VBCSharp/CsCsrefQueryKeywords#20)]  
  
## Example  
 The following example performs a primary sort on the students' last names, and then a secondary sort on their first names.  
  
 [!CODE [cscsrefQueryKeywords#22](../CodeSnippet/VS_Snippets_VBCSharp/CsCsrefQueryKeywords#22)]  
  
## Remarks  
 At compile time, the `orderby` clause is translated to a call to the <xref:System.Linq.Enumerable.OrderBy``2?qualifyHint=False> method. Multiple keys in the `orderby` clause translate to <xref:System.Linq.Enumerable.ThenBy``2?qualifyHint=False> method calls.  
  
## See Also  
 [C# Reference](../vs140/C#-Reference.md)   
 [Query Keywords (C# Reference)](../vs140/Query-Keywords--C#-Reference-.md)   
 [LINQ Query Expressions (C# Programming Guide)](../Topic/LINQ%20Query%20Expressions%20\(C%23%20Programming%20Guide\).md)   
 [group clause (C# Reference)](../Topic/group%20clause%20\(C%23%20Reference\).md)   
 [Getting Started with LINQ in C#](../vs140/Getting-Started-with-LINQ-in-C#.md)