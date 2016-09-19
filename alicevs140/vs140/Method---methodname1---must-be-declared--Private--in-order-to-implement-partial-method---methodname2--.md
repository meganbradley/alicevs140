---
title: "Method &#39;&lt;methodname1&gt;&#39; must be declared &#39;Private&#39; in order to implement partial method &#39;&lt;methodname2&gt;&#39;"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 4d8d19ad-0c3b-4eba-ada8-2cfa6ae795c4
caps.latest.revision: 7
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Method &#39;&lt;methodname1&gt;&#39; must be declared &#39;Private&#39; in order to implement partial method &#39;&lt;methodname2&gt;&#39;
The implementation of a partial method must be declared `Private`. For example, the following code causes this error.  
  
```vb#  
Partial Class Product  
  
    ' Declaration of the partial method.  
    Partial Private Sub valueChanged()  
    End Sub  
  
End Class  
```  
  
```vb#  
Partial Class Product  
  
    ' Implementation of the partial method, with Private missing,   
    ' causes this error.   
    'Sub valueChanged()  
    '    MsgBox(Value was changed to " & Me.Quantity)  
    'End Sub  
  
End Class  
```  
  
 **Error ID:** BC31441  
  
### To correct this error  
  
1.  Use the access modifier `Private` in the implementation of the partial method, as shown in the following example.  
  
    ```vb#  
    Private Sub valueChanged()  
        MsgBox(Value was changed to " & Me.Quantity)  
    End Sub  
    ```  
  
## See Also  
 [Partial Methods](../vs140/Partial-Methods--Visual-Basic-.md)   
 [Access Levels in Visual Basic](../vs140/Access-Levels-in-Visual-Basic.md)