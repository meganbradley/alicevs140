---
title: "How to: Handle Null Values in Query Expressions (C# Programming Guide)"
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
ms.assetid: cb34f7a1-7ef5-466a-90ba-91da30ab525d
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Handle Null Values in Query Expressions (C# Programming Guide)
This example shows how to handle possible null values in source collections. An object collection such as an <xref:System.Collections.Generic.IEnumerable`1?qualifyHint=False> can contain elements whose value is [null](../vs140/null--C#-Reference-.md). If a source collection is null or contains an element whose value is null, and your query does not handle null values, a <xref:System.NullReferenceException?qualifyHint=False> will be thrown when you execute the query.  
  
## Example  
 You can code defensively to avoid a null reference exception as shown in the following example:  
  
 [!CODE [csProgGuideLINQ#82](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideLINQ#82)]  
  
 In the previous example, the `where` clause filters out all null elements in the categories sequence. This technique is independent of the null check in the join clause. The conditional expression with null in this example works because `Products.CategoryID` is of type `int?` which is shorthand for `Nullable<int>`.  
  
## Example  
 In a join clause, if only one of the comparison keys is a nullable value type, you can cast the other to a nullable type in the query expression. In the following example, assume that `EmployeeID` is a column that contains values of type `int?`:  
  
 [!CODE [csProgGuideLINQ#83](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideLINQ#83)]  
  
## See Also  
 <xref:System.Nullable`1?qualifyHint=False>   
 [LINQ Query Expressions (C# Programming Guide)](../Topic/LINQ%20Query%20Expressions%20\(C%23%20Programming%20Guide\).md)   
 [Nullable Types (C# Programming Guide)](../Topic/Nullable%20Types%20\(C%23%20Programming%20Guide\).md)