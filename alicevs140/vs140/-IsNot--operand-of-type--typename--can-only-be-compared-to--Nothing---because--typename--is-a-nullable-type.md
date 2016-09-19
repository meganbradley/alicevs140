---
title: "&#39;IsNot&#39; operand of type &#39;typename&#39; can only be compared to &#39;Nothing&#39;, because &#39;typename&#39; is a nullable type"
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
ms.assetid: 1155b23a-ad75-4bab-b9da-73f35c767a36
caps.latest.revision: 7
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &#39;IsNot&#39; operand of type &#39;typename&#39; can only be compared to &#39;Nothing&#39;, because &#39;typename&#39; is a nullable type
A variable declared as nullable has been compared to an expression other than `Nothing` using the `IsNot` operator.  
  
 **Error ID:** BC32128  
  
### To correct this error  
  
1.  To compare a nullable type to an expression other than `Nothing` by using the `IsNot` operator, call the `GetType` method on the nullable type and compare the result to the expression, as shown in the following example.  
  
    ```vb#  
    Dim number? As Integer = 5  
  
    If number IsNot Nothing Then  
      If number.GetType() IsNot Type.GetType("System.Int32") Then   
  
      End If  
    End If  
    ```  
  
## See Also  
 [Nullable Value Types](../Topic/Nullable%20Value%20Types%20\(Visual%20Basic\).md)   
 [IsNot Operator](../vs140/IsNot-Operator--Visual-Basic-.md)