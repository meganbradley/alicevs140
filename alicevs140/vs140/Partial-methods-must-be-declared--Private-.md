---
title: "Partial methods must be declared &#39;Private&#39;"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 3a4474d9-661e-4793-9624-30cf81faddcf
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Partial methods must be declared &#39;Private&#39;
The access modifier `Private` is required in partial method declarations. The following example shows the use of `Private` in the method signature and its implementation.  
  
```vb#  
' Definition of the partial method signature.  
Partial Private Sub OnNameChanged()  
    ' The body of the signature is empty.  
End Sub  
```  
  
```vb#  
' Implementation of the partial method.  
Private Sub OnNameChanged()  
    MsgBox("Name was changed to " & Me.Name)  
End Sub  
```  
  
 **Error ID:** BC31432  
  
### To correct this error  
  
-   Add the keyword `Private` before `Sub` in the signature and implementation declarations.  
  
## See Also  
 [Partial Methods](../vs140/Partial-Methods--Visual-Basic-.md)