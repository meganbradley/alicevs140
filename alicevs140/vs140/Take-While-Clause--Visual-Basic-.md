---
title: "Take While Clause (Visual Basic)"
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
ms.assetid: db8f9f2f-fc9f-4a6c-b0b8-1bf048147e11
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Take While Clause (Visual Basic)
Includes elements in a collection as long as a specified condition is `true` and bypasses the remaining elements.  
  
## Syntax  
  
```  
Take While expression  
```  
  
## Parts  
  
|||  
|-|-|  
|Term|Definition|  
|`expression`|Required. An expression that represents a condition to test elements for. The expression must return a `Boolean` value or a functional equivalent, such as an `Integer` to be evaluated as a `Boolean`.|  
  
## Remarks  
 The `Take While` clause includes elements from the start of a query result until the supplied `expression` returns `false`. After the `expression` returns `false`, the query will bypass all remaining elements. The `expression` is ignored for the remaining results.  
  
 The `Take While` clause differs from the `Where` clause in that the `Where` clause can be used to include all elements from a query that meet a particular condition. The `Take While` clause includes elements only until the first time that the condition is not satisfied. The `Take While` clause is most useful when you are working with an ordered query result.  
  
## Example  
 The following code example uses the `Take While` clause to retrieve results until the first customer without any orders is found.  
  
 [!CODE [VbSimpleQuerySamples#2](../CodeSnippet/VS_Snippets_VBCSharp/VbSimpleQuerySamples#2)]  
  
## See Also  
 [Introduction to LINQ in Visual Basic](../Topic/Introduction%20to%20LINQ%20in%20Visual%20Basic.md)   
 [Queries (Visual Basic)](../vs140/Queries--Visual-Basic-.md)   
 [Select Clause](../Topic/Select%20Clause%20\(Visual%20Basic\).md)   
 [From Clause](../vs140/From-Clause--Visual-Basic-.md)   
 [Take Clause](../vs140/Take-Clause--Visual-Basic-.md)   
 [Skip While Clause](../vs140/Skip-While-Clause--Visual-Basic-.md)   
 [Where Clause](../vs140/Where-Clause--Visual-Basic-.md)