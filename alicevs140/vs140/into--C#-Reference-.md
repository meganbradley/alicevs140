---
title: "into (C# Reference)"
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
ms.assetid: 81ec62c1-f0b1-4755-8a31-959876e77f65
caps.latest.revision: 20
translation.priority.ht: 
  - de-de
  - ja-jp
---
# into (C# Reference)
The `into` contextual keyword can be used to create a temporary identifier to store the results of a [group](../Topic/group%20clause%20\(C%23%20Reference\).md), [join](../Topic/join%20clause%20\(C%23%20Reference\).md) or [select](../vs140/select-clause--C#-Reference-.md) clause into a new identifier. This identifier can itself be a generator for additional query commands. When used in a `group` or `select` clause, the use of the new identifier is sometimes referred to as a *continuation*.  
  
## Example  
 The following example shows the use of the `into` keyword to enable a temporary identifier `fruitGroup` which has an inferred type of `IGrouping`. By using the identifier, you can invoke the <xref:System.Linq.Enumerable.Count``1?qualifyHint=False> method on each group and select only those groups that contain two or more words.  
  
 [!CODE [cscsrefQueryKeywords#18](../CodeSnippet/VS_Snippets_VBCSharp/CsCsrefQueryKeywords#18)]  
  
 The use of `into` in a `group` clause is only necessary when you want to perform additional query operations on each group. For more information, see [group clause (C# Reference)](../Topic/group%20clause%20\(C%23%20Reference\).md).  
  
 For an example of the use of `into` in a `join` clause, see [join clause (C# Reference)](../Topic/join%20clause%20\(C%23%20Reference\).md).  
  
## See Also  
 [Query Keywords (C# Reference)](../vs140/Query-Keywords--C#-Reference-.md)   
 [LINQ Query Expressions (C# Programming Guide)](../Topic/LINQ%20Query%20Expressions%20\(C%23%20Programming%20Guide\).md)   
 [group clause (C# Reference)](../Topic/group%20clause%20\(C%23%20Reference\).md)