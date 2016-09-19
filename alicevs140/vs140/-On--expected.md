---
title: "&#39;On&#39; expected"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 7cb1b205-c4c3-4485-ae3f-8942425692ff
caps.latest.revision: 7
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &#39;On&#39; expected
A `Join` or `Group Join` clause has been specified without an `On` operator. You use the `On` operator to identify the key field of the range variable for each collection. Key fields are used to match items from each collection.  
  
 **Error ID:** BC36618  
  
### To correct this error  
  
1.  Add the `On` operator and key fields to the `Join` or `Group Join` clause. Following is an example:  
  
    ```vb#  
    Dim petOwnersJoin = From pers In people _  
                        Join pet In pets _  
                        On pet.Owner Equals pers _  
                        Select pers.FirstName, PetName = pet.Name  
    ```  
  
## See Also  
 [How To: Combine Data with LINQ by Using Joins (Visual Basic)](../vs140/How-to--Combine-Data-with-LINQ-by-Using-Joins--Visual-Basic-.md)   
 [Join Clause (Visual Basic)](../vs140/Join-Clause--Visual-Basic-.md)   
 [Group Join Clause (Visual Basic)](../vs140/Group-Join-Clause--Visual-Basic-.md)   
 [Introduction to LINQ in Visual Basic](../Topic/Introduction%20to%20LINQ%20in%20Visual%20Basic.md)   
 [LINQ in Visual Basic](../vs140/LINQ-in-Visual-Basic.md)