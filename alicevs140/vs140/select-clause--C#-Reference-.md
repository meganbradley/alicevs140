---
title: "select clause (C# Reference)"
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
ms.assetid: df01e266-5781-4aaa-80c4-67cf28ea093f
caps.latest.revision: 21
translation.priority.ht: 
  - de-de
  - ja-jp
---
# select clause (C# Reference)
In a query expression, the `select` clause specifies the type of values that will be produced when the query is executed. The result is based on the evaluation of all the previous clauses and on any expressions in the `select` clause itself. A query expression must terminate with either a `select` clause or a [group](../Topic/group%20clause%20\(C%23%20Reference\).md) clause.  
  
 The following example shows a simple `select` clause in a query expression.  
  
 [!CODE [cscsrefQueryKeywords#8](../CodeSnippet/VS_Snippets_VBCSharp/CsCsrefQueryKeywords#8)]  
  
 The type of the sequence produced by the `select` clause determines the type of the query variable `queryHighScores`. In the simplest case, the `select` clause just specifies the range variable. This causes the returned sequence to contain elements of the same type as the data source. For more information, see [Type Relationships in Query Operations (LINQ)](../vs140/Type-Relationships-in-LINQ-Query-Operations--C#-.md). However, the `select` clause also provides a powerful mechanism for transforming (or *projecting*) source data into new types. For more information, see [Data Transformations with LINQ](../vs140/Data-Transformations-with-LINQ--C#-.md).  
  
## Example  
 The following example shows all the different forms that a `select` clause may take. In each query, note the relationship between the `select` clause and the type of the *query variable* (`studentQuery1`, `studentQuery2`, and so on).  
  
 [!CODE [cscsrefQueryKeywords#9](../CodeSnippet/VS_Snippets_VBCSharp/CsCsrefQueryKeywords#9)]  
  
 As shown in `studentQuery8` in the previous example, sometimes you might want the elements of the returned sequence to contain only a subset of the properties of the source elements. By keeping the returned sequence as small as possible you can reduce the memory requirements and increase the speed of the execution of the query. You can accomplish this by creating an anonymous type in the `select` clause and using an object initializer to initialize it with the appropriate properties from the source element. For an example of how to do this, see [Object and Collection Initializers (C# Programming Guide)](../Topic/Object%20and%20Collection%20Initializers%20\(C%23%20Programming%20Guide\).md).  
  
## Remarks  
 At compile time, the `select` clause is translated to a method call to the <xref:System.Linq.Enumerable.Select``2?qualifyHint=False> standard query operator.  
  
## See Also  
 [C# Reference](../vs140/C#-Reference.md)   
 [Query Keywords (C# Reference)](../vs140/Query-Keywords--C#-Reference-.md)   
 [from clause(C# Reference)](../Topic/from%20clause%20\(C%23%20Reference\).md)   
 [where clause (C# Reference)](../vs140/partial--Method---C#-Reference-.md)   
 [Anonymous Types (C# Programming Guide)](../Topic/Anonymous%20Types%20\(C%23%20Programming%20Guide\).md)   
 [LINQ Query Expressions (C# Programming Guide)](../Topic/LINQ%20Query%20Expressions%20\(C%23%20Programming%20Guide\).md)   
 [Getting Started with LINQ in C#](../vs140/Getting-Started-with-LINQ-in-C#.md)