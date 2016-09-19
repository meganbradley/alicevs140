---
title: "&#39;By&#39; expected"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: d0397b6e-bfc2-400c-92fc-efe82036cfdb
caps.latest.revision: 6
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &#39;By&#39; expected
An `Order By` or `Group By` clause has been specified without the `By` keyword.  
  
 **Error ID:** BC36605  
  
### To correct this error  
  
1.  Add the `By` keyword to the `Order By` or `Group By` clause. The following is an example:  
  
    ```vb#  
    Dim customersByCountry = From cust In customers _  
                             Order By cust.Country, cust.City _  
                             Group By CountryName = cust.Country _  
                             Into RegionalCustomers = Group, Count() _  
                             Order By CountryName  
    ```  
  
## See Also  
 [How To: Sort a Collection by Using LINQ (Visual Basic)](../Topic/How%20to:%20Sort%20Query%20Results%20by%20Using%20LINQ%20\(Visual%20Basic\).md)   
 [Order By Clause (Visual Basic)](../vs140/Order-By-Clause--Visual-Basic-.md)   
 [Group By Clause (Visual Basic)](../vs140/Group-By-Clause--Visual-Basic-.md)   
 [Introduction to LINQ in Visual Basic](../Topic/Introduction%20to%20LINQ%20in%20Visual%20Basic.md)   
 [LINQ in Visual Basic](../vs140/LINQ-in-Visual-Basic.md)