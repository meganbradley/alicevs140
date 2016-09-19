---
title: "&#39;Equals&#39; expected"
ms.custom: na
ms.date: 09/18/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 1fd8c0dc-0e87-47b7-ab30-498809cca033
caps.latest.revision: 5
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &#39;Equals&#39; expected
A `Join` or `Group Join` clause has been specified without an `Equals` operator. You use the `Equals` operator to identify the `Boolean` operation to test key fields for matching items.  
  
 **Error ID:** BC36619  
  
### To correct this error  
  
1.  Add the `Equals` operator and key fields to the `Join` or `Group Join` clause. For example:  
  
    ```vb#  
    Dim petOwnersGrouped = From pers In people _  
                           Group Join pet In pets _  
                             On pers Equals pet.Owner _  
                           Into PetList = Group _  
                           Select pers.FirstName, pers.LastName, _  
                                  PetList  
    ```  
  
## See Also  
 [How To: Combine Data with LINQ by Using Joins (Visual Basic)](../vs140/How-to--Combine-Data-with-LINQ-by-Using-Joins--Visual-Basic-.md)   
 [Join Clause (Visual Basic)](../vs140/Join-Clause--Visual-Basic-.md)   
 [Group Join Clause (Visual Basic)](../vs140/Group-Join-Clause--Visual-Basic-.md)   
 [Introduction to LINQ in Visual Basic](../Topic/Introduction%20to%20LINQ%20in%20Visual%20Basic.md)   
 [LINQ in Visual Basic](../vs140/LINQ-in-Visual-Basic.md)