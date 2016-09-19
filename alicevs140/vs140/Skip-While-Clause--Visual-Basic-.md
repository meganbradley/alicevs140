---
title: "Skip While Clause (Visual Basic)"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - VB
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-visual-basic
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 5dee8350-7520-4f1a-b00d-590cacd572d6
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Skip While Clause (Visual Basic)
Bypasses elements in a collection as long as a specified condition is `true` and then returns the remaining elements.  
  
## Syntax  
  
```  
Skip While expression  
```  
  
## Parts  
  
|||  
|-|-|  
|Term|Definition|  
|`expression`|Required. An expression that represents a condition to test elements for. The expression must return a `Boolean` value or a functional equivalent, such as an `Integer` to be evaluated as a `Boolean`.|  
  
## Remarks  
 The `Skip While` clause bypasses elements from the beginning of a query result until the supplied `expression` returns `false`. After `expression` returns `false`, the query returns all the remaining elements. The `expression` is ignored for the remaining results.  
  
 The `Skip While` clause differs from the `Where` clause in that the `Where` clause can be used to exclude all elements from a query that do not meet a particular condition. The `Skip While` clause excludes elements only until the first time that the condition is not satisfied. The `Skip While` clause is most useful when you are working with an ordered query result.  
  
 You can bypass a specific number of results from the beginning of a query result by using the `Skip` clause.  
  
## Example  
 The following code example uses the `Skip While` clause to bypass results until the first customer from the United States is found.  
  
 [!CODE [VbSimpleQuerySamples#3](../CodeSnippet/VS_Snippets_VBCSharp/VbSimpleQuerySamples#3)]  
  
## See Also  
 [Introduction to LINQ in Visual Basic](../Topic/Introduction%20to%20LINQ%20in%20Visual%20Basic.md)   
 [Queries (Visual Basic)](../vs140/Queries--Visual-Basic-.md)   
 [Select Clause](../Topic/Select%20Clause%20\(Visual%20Basic\).md)   
 [From Clause](../vs140/From-Clause--Visual-Basic-.md)   
 [Skip Clause (Visual Basic)](../vs140/Skip-Clause--Visual-Basic-.md)   
 [Take While Clause (Visual Basic)](../vs140/Take-While-Clause--Visual-Basic-.md)   
 [Where Clause](../vs140/Where-Clause--Visual-Basic-.md)