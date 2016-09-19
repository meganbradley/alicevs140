---
title: "Order By Clause (Visual Basic)"
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
ms.assetid: fa911282-6b81-44c7-acfa-46b5bb93df75
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Order By Clause (Visual Basic)
Specifies the sort order for a query result.  
  
## Syntax  
  
```  
Order By orderExp1 [ Ascending | Descending ] [, orderExp2 [...] ]  
```  
  
## Parts  
 `orderExp1`  
 Required. One or more fields from the current query result that identify how to order the returned values. The field names must be separated by commas (,). You can identify each field as sorted in ascending or descending order by using the `Ascending` or `Descending` keywords. If no `Ascending` or `Descending` keyword is specified, the default sort order is ascending. The sort order fields are given precedence from left to right.  
  
## Remarks  
 You can use the `Order By` clause to sort the results of a query. The `Order By` clause can only sort a result based on the range variable for the current scope. For example, the `Select` clause introduces a new scope in a query expression with new iteration variables for that scope. Range variables defined before a `Select` clause in a query are not available after the `Select` clause. Therefore, if you want to order your results by a field that is not available in the `Select` clause, you must put the `Order By` clause before the `Select` clause. One example of when you would have to do this is when you want to sort your query by fields that are not returned as part of the result.  
  
 Ascending and descending order for a field is determined by the implementation of the <xref:System.IComparable?qualifyHint=False> interface for the data type of the field. If the data type does not implement the <xref:System.IComparable?qualifyHint=False> interface, the sort order is ignored.  
  
## Example  
 The following query expression uses a `From` clause to declare a range variable `book` for the `books` collection. The `Order By` clause sorts the query result by price in ascending order (the default). Books with the same price are sorted by title in ascending order. The `Select` clause selects the `Title` and `Price` properties as the values returned by the query.  
  
 [!CODE [VbSimpleQuerySamples#24](../CodeSnippet/VS_Snippets_VBCSharp/VbSimpleQuerySamples#24)]  
  
## Example  
 The following query expression uses the `Order By` clause to sort the query result by price in descending order. Books with the same price are sorted by title in ascending order.  
  
 [!CODE [VbSimpleQuerySamples#25](../CodeSnippet/VS_Snippets_VBCSharp/VbSimpleQuerySamples#25)]  
  
## Example  
 The following query expression uses a `Select` clause to select the book title, price, publish date, and author. It then populates the `Title`, `Price`, `PublishDate`, and `Author` fields of the range variable for the new scope. The `Order By` clause orders the new range variable by author name, book title, and then price. Each column is sorted in the default order (ascending).  
  
 [!CODE [VbSimpleQuerySamples#26](../CodeSnippet/VS_Snippets_VBCSharp/VbSimpleQuerySamples#26)]  
  
## See Also  
 [Introduction to LINQ in Visual Basic](../Topic/Introduction%20to%20LINQ%20in%20Visual%20Basic.md)   
 [Queries (Visual Basic)](../vs140/Queries--Visual-Basic-.md)   
 [Select Clause](../Topic/Select%20Clause%20\(Visual%20Basic\).md)   
 [From Clause](../vs140/From-Clause--Visual-Basic-.md)