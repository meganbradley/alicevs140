---
title: "Lambda expressions are not valid in the first expression of a &#39;Select Case&#39; statement"
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
ms.assetid: 74609979-9c03-4864-bbce-f588aa2e0917
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Lambda expressions are not valid in the first expression of a &#39;Select Case&#39; statement
You cannot use a lambda expression for the test expression in a `Select Case` statement. Lambda expression definitions return functions, and the test expression of a `Select Case` statement must be an elementary data type.  
  
 The following code causes this error:  
  
```vb#  
' Select Case (Function(arg) arg Is Nothing)  
    ' List of the cases.  
' End Select  
```  
  
 **Error ID:** BC36635  
  
### To correct this error  
  
-   Examine your code to determine whether a different conditional construction, such as an `If...Then...Else` statement, would work for you.  
  
-   You may have intended to call the function, as shown in the following code:  
  
    ```vb#  
    Dim num? As Integer  
    Select Case ((Function(arg? As Integer) arg Is Nothing)(num))  
        ' List of the cases  
    End Select  
    ```  
  
## See Also  
 [Lambda Expressions](../vs140/Lambda-Expressions--Visual-Basic-.md)   
 [If...Then...Else Statement](../Topic/If...Then...Else%20Statement%20\(Visual%20Basic\).md)   
 [Select...Case Statement (Visual Basic)](../Topic/Select...Case%20Statement%20\(Visual%20Basic\).md)