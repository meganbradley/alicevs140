---
title: "Method &#39;&lt;methodname1&gt;&#39; cannot implement partial method &#39;&lt;methodname2&gt;&#39; because &#39;&lt;methodname3&gt;&#39; already implements it"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 61cba19e-db11-4a06-89d6-4244d411588c
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Method &#39;&lt;methodname1&gt;&#39; cannot implement partial method &#39;&lt;methodname2&gt;&#39; because &#39;&lt;methodname3&gt;&#39; already implements it
Method '<methodname1\>' cannot implement partial method '<methodname2\>' because '<methodname3\>' already implements it. Only one method can implement a partial method.  
  
 You cannot have two partial methods that implement the same partial method declaration. The following code causes this error.  
  
```vb#  
Partial Class Product  
  
    ' Declaration of the partial method.  
    Partial Private Sub ValueChanged()  
    End Sub  
  
End Class  
```  
  
```vb#  
Partial Class Product  
  
    ' First implementation of the partial method.  
    Private Sub ValueChanged()  
        MsgBox(Value was changed to " & Me.Quantity)  
    End Sub  
  
    ' Second implementation of the partial method causes this error.  
    'Private Sub ValueChanged()  
    '    Console.WriteLine("Quantity was changed to " & Me.Quantity)  
    'End Sub  
  
End Class  
```  
  
 **Error ID:** BC31434  
  
## See Also  
 [Partial Methods](../vs140/Partial-Methods--Visual-Basic-.md)