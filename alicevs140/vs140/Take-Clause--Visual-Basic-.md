---
title: "Take Clause (Visual Basic)"
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
ms.assetid: 77bf87b2-1476-4456-957f-fee922fbad8c
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Take Clause (Visual Basic)
Returns a specified number of contiguous elements from the start of a collection.  
  
## Syntax  
  
```  
Take count  
```  
  
## Parts  
 `count`  
 Required. A value or an expression that evaluates to the number of elements of the sequence to return.  
  
## Remarks  
 The `Take` clause causes a query to include a specified number of contiguous elements from the start of a results list. The number of elements to include is specified by the `count` parameter.  
  
 You can use the `Take` clause with the `Skip` clause to return a range of data from any segment of a query. To do this, pass the index of the first element of the range to the `Skip` clause and the size of the range to the `Take` clause. In this case, the `Take` clause must be specified after the `Skip` clause.  
  
 When you use the `Take` clause in a query, you may also need to ensure that the results are returned in an order that will enable the `Take` clause to include the intended results. For more information about ordering query results, see [Order By Clause (Visual Basic)](../vs140/Order-By-Clause--Visual-Basic-.md).  
  
 You can use the `TakeWhile` clause to specify that only certain elements be returned, depending on a supplied condition.  
  
## Example  
 The following code example uses the `Take` clause together with the `Skip` clause to return data from a query in pages. The GetCustomers function uses the `Skip` clause to bypass the customers in the list until the supplied starting index value, and uses the `Take` clause to return a page of customers starting from that index value.  
  
 [!CODE [VbSimpleQuerySamples#1](../CodeSnippet/VS_Snippets_VBCSharp/VbSimpleQuerySamples#1)]  
  
## See Also  
 [Introduction to LINQ in Visual Basic](../Topic/Introduction%20to%20LINQ%20in%20Visual%20Basic.md)   
 [Queries (Visual Basic)](../vs140/Queries--Visual-Basic-.md)   
 [Select Clause](../Topic/Select%20Clause%20\(Visual%20Basic\).md)   
 [From Clause](../vs140/From-Clause--Visual-Basic-.md)   
 [Order By Clause (Visual Basic)](../vs140/Order-By-Clause--Visual-Basic-.md)   
 [Take While Clause (Visual Basic)](../vs140/Take-While-Clause--Visual-Basic-.md)   
 [Skip Clause (Visual Basic)](../vs140/Skip-Clause--Visual-Basic-.md)