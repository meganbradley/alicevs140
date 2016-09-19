---
title: "Where Clause (Visual Basic)"
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
ms.assetid: 48b5c2c5-3181-429c-8545-894296798c89
caps.latest.revision: 20
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Where Clause (Visual Basic)
Specifies the filtering condition for a query.  
  
## Syntax  
  
```  
Where condition  
```  
  
## Parts  
 `condition`  
 Required. An expression that determines whether the values for the current item in the collection are included in the output collection. The expression must evaluate to a `Boolean` value or the equivalent of a `Boolean` value. If the condition evaluates to `True`, the element is included in the query result; otherwise, the element is excluded from the query result.  
  
## Remarks  
 The `Where` clause enables you to filter query data by selecting only elements that meet certain criteria. Elements whose values cause the `Where` clause to evaluate to `True` are included in the query result; other elements are excluded. The expression that is used in a `Where` clause must evaluate to a `Boolean` or the equivalent of a `Boolean`, such as an Integer that evaluates to `False` when its value is zero. You can combine multiple expressions in a `Where` clause by using logical operators such as `And`, `Or`, `AndAlso`, `OrElse`, `Is`, and `IsNot`.  
  
 By default, query expressions are not evaluated until they are accessed—for example, when they are data-bound or iterated through in a `For` loop. As a result, the `Where` clause is not evaluated until the query is accessed. If you have values external to the query that are used in the `Where` clause, ensure that the appropriate value is used in the `Where` clause at the time the query is executed. For more information about query execution, see [Three Stages of a LINQ Query (Visual Basic)](../Topic/Writing%20Your%20First%20LINQ%20Query%20\(Visual%20Basic\).md).  
  
 You can call functions within a `Where` clause to perform a calculation or operation on a value from the current element in the collection. Calling a function in a `Where` clause can cause the query to be executed immediately when it is defined instead of when it is accessed. For more information about query execution, see [Three Stages of a LINQ Query (Visual Basic)](../Topic/Writing%20Your%20First%20LINQ%20Query%20\(Visual%20Basic\).md).  
  
## Example  
 The following query expression uses a `From` clause to declare a range variable `cust` for each `Customer` object in the `customers` collection. The `Where` clause uses the range variable to restrict the output to customers from the specified region. The `For Each` loop displays the company name for each customer in the query result.  
  
 [!CODE [VbSimpleQuerySamples#23](../CodeSnippet/VS_Snippets_VBCSharp/VbSimpleQuerySamples#23)]  
  
## Example  
 The following example uses `And` and `Or` logical operators in the `Where` clause.  
  
 [!CODE [VbSimpleQuerySamples#31](../CodeSnippet/VS_Snippets_VBCSharp/VbSimpleQuerySamples#31)]  
  
## See Also  
 [Introduction to LINQ in Visual Basic](../Topic/Introduction%20to%20LINQ%20in%20Visual%20Basic.md)   
 [Queries (Visual Basic)](../vs140/Queries--Visual-Basic-.md)   
 [From Clause](../vs140/From-Clause--Visual-Basic-.md)   
 [Select Clause](../Topic/Select%20Clause%20\(Visual%20Basic\).md)   
 [For Each...Next Statement (Visual Basic)](../Topic/For%20Each...Next%20Statement%20\(Visual%20Basic\).md)