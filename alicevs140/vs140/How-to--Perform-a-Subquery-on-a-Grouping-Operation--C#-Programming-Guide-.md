---
title: "How to: Perform a Subquery on a Grouping Operation (C# Programming Guide)"
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
ms.assetid: 7b0805cd-53b4-429d-86b6-d37fb08f2c95
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Perform a Subquery on a Grouping Operation (C# Programming Guide)
This topic shows two different ways to create a query that orders the source data into groups, and then performs a subquery over each group individually. The basic technique in each example is to group the source elements by using a *continuation* named `newGroup`, and then generating a new subquery against `newGroup`. This subquery is run against each new group that is created by the outer query. Note that in this particular example the final output is not a group, but a flat sequence of anonymous types.  
  
 For more information about how to group, see [group clause (C# Reference)](../Topic/group%20clause%20\(C%23%20Reference\).md).  
  
 For more information about continuations, see [into (C# Reference)](../vs140/into--C#-Reference-.md). The following example uses an in-memory data structure as the data source, but the same principles apply for any kind of [!INCLUDE[vbteclinq](../vs140/includes/vbteclinq_md.md)] data source.  
  
## Example  
 [!CODE [csProgGuideLINQ#23](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideLINQ#23)]  
  
## Compiling the Code  
 This example contains references to objects that are defined in the sample application in [How to: Query a Collections of Objects](../vs140/How-to--Query-a-Collection-of-Objects--C#-Programming-Guide-.md). To compile and run this method, paste it into the `StudentClass` class in that application and add a call to it from the `Main` method.  
  
 When you adapt this method to your own application, remember that LINQ requires version 3.5 of the [!INCLUDE[dnprdnshort](../vs140/includes/dnprdnshort_md.md)], and the project must contain a reference to System.Core.dll and a using directive for System.Linq. LINQ to SQL, LINQ to XML and LINQ to DataSet types require additional usings and references. For more information, see [How To: Create a LINQ Project](../vs140/How-to--Create-a-LINQ-Project.md).  
  
## See Also  
 [LINQ Query Expressions (C# Programming Guide)](../Topic/LINQ%20Query%20Expressions%20\(C%23%20Programming%20Guide\).md)