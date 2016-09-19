---
title: "Property &#39;&lt;propertyname&gt;&#39; cannot be initialized in an object initializer expression because all accessible overloads require arguments"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: d4476065-2ca2-4c9e-a571-c08917a6387f
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Property &#39;&lt;propertyname&gt;&#39; cannot be initialized in an object initializer expression because all accessible overloads require arguments
The members initialized in an object initializer list must be either fields or properties. Additionally, properties in an initializer list cannot have parameters. The property causing this error is overloaded, and each of its versions requires arguments. Therefore, the property cannot be initialized in an object initializer list.  
  
 **Error ID:** BC30993  
  
### To correct this error  
  
-   Remove the property that requires arguments from the initializer list.  
  
## Example  
 The following class contains three property definitions: one for `TotalItems` and two for `Item`, which is overloaded.  
  
```  
Class CollectionOfItems  
    Property TotalItems() As Integer  
        Get  
        End Get  
        Set(ByVal value As Integer)  
        End Set  
    End Property  
    Property Item(ByVal Key As String) As Object  
        Get  
        End Get  
        Set(ByVal value As Object)  
        End Set  
    End Property  
    Property Item(ByVal Index As Integer) As Object  
        Get  
        End Get  
        Set(ByVal value As Object)  
        End Set  
    End Property  
End Class  
```  
  
 The `TotalItems` property requires no arguments and can be initialized in an object initialization list, as shown in the following declaration.  
  
```  
Dim coinCollection As New CollectionOfItems With { .TotalItems = 0 }  
```  
  
 The `Item` property is overloaded, and each overload requires an argument. Therefore, `Item` cannot appear in an object initializer list.  
  
```  
' The following declaration is not valid.  
' Dim coinCollection As New CollectionOfItems With { .TotalItems = 0, _  
'    .Item = aCoinObject }  
```  
  
 To avoid this error, initialize the `Item` property outside the object initializer.  
  
```  
Dim coinCollection As New CollectionOfItems With { .TotalItems = 0 }  
coinCollection.Item(1) = aCoinObject  
```  
  
## See Also  
 [NOT IN BUILD: Properties and Property Procedures](assetId:///23e2a1ec-7e9d-4109-8940-c703d981077b)   
 [Object Initializers](../vs140/Object-Initializers--Named-and-Anonymous-Types--Visual-Basic-.md)   
 [How to: Call a Property Procedure](../vs140/How-to--Call-a-Property-Procedure--Visual-Basic-.md)   
 [NOT IN BUILD: Default Properties](assetId:///a70f2a27-8176-4858-935e-f25afdd43ab5)   
 [Overloads](../vs140/Overloads--Visual-Basic-.md)   
 [Procedure Overloading](../Topic/Procedure%20Overloading%20\(Visual%20Basic\).md)