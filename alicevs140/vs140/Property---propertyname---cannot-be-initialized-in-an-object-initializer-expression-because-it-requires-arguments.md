---
title: "Property &#39;&lt;propertyname&gt;&#39; cannot be initialized in an object initializer expression because it requires arguments"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: a4d050b2-7366-457a-a852-8eb490c97573
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Property &#39;&lt;propertyname&gt;&#39; cannot be initialized in an object initializer expression because it requires arguments
The members initialized in an object initializer list must be fields or properties, and property members cannot have parameters. For example, default properties require arguments, so they cannot be initialized in an object initializer list. For more information, see [NOT IN BUILD: Default Properties](assetId:///a70f2a27-8176-4858-935e-f25afdd43ab5).  
  
 **Error ID:** BC30992  
  
### To correct this error  
  
-   Remove from the initialization list all properties that have arguments.  
  
## Example  
 The following class contains a default property, `defaultProp`, that requires an integer argument.  
  
```  
Public Class SomeStrings  
    Private myStrings() As String  
    Sub New(ByVal size As Integer)  
        ReDim myStrings(size)  
    End Sub  
    Default Property defaultProp(ByVal index As Integer) As String  
        Get  
            Return myStrings(index)  
        End Get  
        Set(ByVal Value As String)  
            myStrings(index) = Value  
        End Set  
    End Property  
End Class  
```  
  
 Because the default property requires an argument, the following declaration causes an error.  
  
```  
' Dim strs As New SomeStrings(2) With { .defaultProp = "One" }  
```  
  
## See Also  
 [NOT IN BUILD: Default Properties](assetId:///a70f2a27-8176-4858-935e-f25afdd43ab5)   
 [NOT IN BUILD: Properties and Property Procedures](assetId:///23e2a1ec-7e9d-4109-8940-c703d981077b)   
 [Object Initializers](../vs140/Object-Initializers--Named-and-Anonymous-Types--Visual-Basic-.md)