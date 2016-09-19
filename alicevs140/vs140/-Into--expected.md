---
title: "&#39;Into&#39; expected"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 24062dd9-a973-43b6-88d3-c11adc5a3736
caps.latest.revision: 7
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &#39;Into&#39; expected
An `Aggregate`, `Group By`, or `Group Join` clause has been specified without an `Into` operator. You use the `Into` operator to identify aggregate functions to apply to the query result and to identify the member of the query result type to contain the grouped results (by using the `Group` aggregate function).  
  
 **Error ID:** BC36615  
  
### To correct this error  
  
1.  Add the `Into` operator to the `Aggregate`, `Group By`, or `Group Join` clause. The following is an example:  
  
    ```vb#  
    Dim orders = From order In orderList _  
                 Order By order.OrderDate _  
                 Group By OrderDate = order.OrderDate _  
                 Into OrdersByDate = Group  
    ```  
  
## See Also  
 [Aggregate Clause (Visual Basic)](../vs140/Aggregate-Clause--Visual-Basic-.md)   
 [Group By Clause (Visual Basic)](../vs140/Group-By-Clause--Visual-Basic-.md)   
 [Group Join Clause (Visual Basic)](../vs140/Group-Join-Clause--Visual-Basic-.md)   
 [Introduction to LINQ in Visual Basic](../Topic/Introduction%20to%20LINQ%20in%20Visual%20Basic.md)   
 [LINQ in Visual Basic](../vs140/LINQ-in-Visual-Basic.md)