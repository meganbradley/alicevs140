---
title: "Skip Clause (Visual Basic)"
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
ms.assetid: f00eb172-3907-4c43-9745-d8546ab86234
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Skip Clause (Visual Basic)
Bypasses a specified number of elements in a collection and then returns the remaining elements.  
  
## Syntax  
  
```  
Skip count  
```  
  
## Parts  
 `count`  
 Required. A value or an expression that evaluates to the number of elements of the sequence to skip.  
  
## Remarks  
 The `Skip` clause causes a query to bypass elements at the beginning of a results list and return the remaining elements. The number of elements to skip is identified by the `count` parameter.  
  
 You can use the `Skip` clause with the `Take` clause to return a range of data from any segment of a query. To do this, pass the index of the first element of the range to the `Skip` clause and the size of the range to the `Take` clause.  
  
 When you use the `Skip` clause in a query, you may also need to ensure that the results are returned in an order that will enable the `Skip` clause to bypass the intended results. For more information about ordering query results, see [Order By Clause (Visual Basic)](../vs140/Order-By-Clause--Visual-Basic-.md).  
  
 You can use the `SkipWhile` clause to specify that only certain elements are ignored, depending on a supplied condition.  
  
## Example  
 The following code example uses the `Skip` clause together with the `Take` clause to return data from a query in pages. The `GetCustomers` function uses the `Skip` clause to bypass the customers in the list until the supplied starting index value, and uses the `Take` clause to return a page of customers starting from that index value.  
  
 [!CODE [VbSimpleQuerySamples#1](../CodeSnippet/VS_Snippets_VBCSharp/VbSimpleQuerySamples#1)]  
  
## See Also  
 [Introduction to LINQ in Visual Basic](../Topic/Introduction%20to%20LINQ%20in%20Visual%20Basic.md)   
 [Queries (Visual Basic)](../vs140/Queries--Visual-Basic-.md)   
 [Select Clause](../Topic/Select%20Clause%20\(Visual%20Basic\).md)   
 [From Clause](../vs140/From-Clause--Visual-Basic-.md)   
 [Order By Clause (Visual Basic)](../vs140/Order-By-Clause--Visual-Basic-.md)   
 [SkipWhile Clause (Visual Basic)](../vs140/Skip-While-Clause--Visual-Basic-.md)   
 [Take Clause (Visual Basic)](../vs140/Take-Clause--Visual-Basic-.md)