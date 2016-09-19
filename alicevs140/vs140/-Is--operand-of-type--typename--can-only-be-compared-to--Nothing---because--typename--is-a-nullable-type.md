---
title: "&#39;Is&#39; operand of type &#39;typename&#39; can only be compared to &#39;Nothing&#39;, because &#39;typename&#39; is a nullable type"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 68b745b5-8605-4bf3-a6ec-69e67b3cff2d
caps.latest.revision: 7
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &#39;Is&#39; operand of type &#39;typename&#39; can only be compared to &#39;Nothing&#39;, because &#39;typename&#39; is a nullable type
A variable declared as nullable has been compared to an expression other than `Nothing` by using the `Is` operator.  
  
 **Error ID:** BC32127  
  
### To correct this error  
  
1.  To compare a nullable type to an expression other than `Nothing` by using the `Is` operator, call the `GetType` method on the nullable type and compare the result to the expression, as shown in the following example.  
  
    ```vb#  
    Dim number? As Integer = 5  
  
    If number IsNot Nothing Then  
      If number.GetType() Is Type.GetType("System.Int32") Then   
  
      End If  
    End If  
    ```  
  
## See Also  
 [Nullable Value Types](../Topic/Nullable%20Value%20Types%20\(Visual%20Basic\).md)   
 [Is Operator (Visual Basic)](../vs140/Is-Operator--Visual-Basic-.md)