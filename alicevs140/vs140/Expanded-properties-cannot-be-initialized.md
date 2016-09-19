---
title: "Expanded properties cannot be initialized"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: ba9408f3-e606-4749-8372-987999f405f5
caps.latest.revision: 6
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Expanded properties cannot be initialized
An auto-implemented property can be initialized as part of its declaration, but an expanded property cannot be.  
  
 **Error ID:** BC36714  
  
### To correct this error  
  
-   Either use an auto-implemented property or remove the initialization from the property declaration.  
  
## Example  
 The following examples show both auto-implemented and expanded properties. Auto-implemented properties can be initialized by using assignment or a `New` clause, but expanded properties cannot be.  
  
```vb#  
Class AutoImplementedExample  
    ' An auto-implemented property can be assigned an initial value.  
    Property IDNum As Integer = 33542  
    ' An auto-implemented property can be initialized with New.  
    Property Name As New String("Don Hall")  
End Class  
  
Class ExpandedExample  
    ' Attempting to expand an initialized auto-implemented property  
    ' causes this error.  
    'Property IDNum As Integer = 33542  
    '    Get  
    '    End Get  
    '    Set(ByVal value As Integer)  
    '    End Set  
    'End Property  
  
    ' Instead, you can assign the initial value to the backing field.  
    Private _IDNum As Integer = 33542  
    Property IDNum As Integer  
        Get  
        End Get  
        Set(ByVal value As Integer)  
        End Set  
    End Property  
End Class  
```  
  
## See Also  
 [Auto-Implemented Properties](../vs140/Auto-Implemented-Properties--Visual-Basic-.md)   
 [How to: Create a Property](../vs140/How-to--Create-a-Property--Visual-Basic-.md)   
 [Property Procedures](../vs140/Property-Procedures--Visual-Basic-.md)