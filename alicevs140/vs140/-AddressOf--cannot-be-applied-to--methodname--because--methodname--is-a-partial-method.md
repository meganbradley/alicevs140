---
title: "&#39;AddressOf&#39; cannot be applied to &#39;methodname&#39; because &#39;methodname&#39; is a partial method"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 924dbada-3e0a-4004-a3ae-a209b7c3d1fa
caps.latest.revision: 6
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &#39;AddressOf&#39; cannot be applied to &#39;methodname&#39; because &#39;methodname&#39; is a partial method
A partial method has been passed to the `AddressOf` operator. Partial methods are invalid values for the `AddressOf` operator.  
  
 **Error ID:** BC31440  
  
### To correct this error  
  
1.  Add an implementation method for the partial method. The implementation method is a valid value for the `AddressOf` operator. The following example shows a partial method signature and its implementation.  
  
    ```vb#  
    ' Definition of the partial method signature.  
    Partial Private Sub OnNameChanged()  
        ' The body of the signature is empty.  
    End Sub  
  
    ' Implementation of the partial method.  
    Private Sub OnNameChanged()  
        MsgBox("Name was changed to " & Me.Name)  
    End Sub  
    ```  
  
## See Also  
 [AddressOf Operator](../vs140/AddressOf-Operator--Visual-Basic-.md)   
 [Partial Methods](../vs140/Partial-Methods--Visual-Basic-.md)