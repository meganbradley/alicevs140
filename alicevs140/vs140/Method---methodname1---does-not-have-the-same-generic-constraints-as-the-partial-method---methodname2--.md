---
title: "Method &#39;&lt;methodname1&gt;&#39; does not have the same generic constraints as the partial method &#39;&lt;methodname2&gt;&#39;"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: ea092f0c-661b-49db-80c1-76401fc8bc0b
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Method &#39;&lt;methodname1&gt;&#39; does not have the same generic constraints as the partial method &#39;&lt;methodname2&gt;&#39;
You have defined a partial method implementation that has generic constraints that differ from the constraints in the partial method declaration. The following code illustrates the error.  
  
```vb#  
Partial Class Class1  
  
    Partial Private Sub Test(Of T As Class)(ByVal arg As T)  
    End Sub  
  
End Class  
  
Partial Class Class1  
  
    '' The error occurs here, for Test.  
    'Private Sub Test(Of T As Structure)(ByVal arg As T)  
    'End Sub  
  
End Class  
```  
  
 **Error ID:** BC31438  
  
## See Also  
 [Partial Methods](../vs140/Partial-Methods--Visual-Basic-.md)   
 [Partial (Visual Basic)](../Topic/Partial%20\(Visual%20Basic\).md)   
 [Generic Procedures in Visual Basic](../vs140/Generic-Procedures-in-Visual-Basic.md)