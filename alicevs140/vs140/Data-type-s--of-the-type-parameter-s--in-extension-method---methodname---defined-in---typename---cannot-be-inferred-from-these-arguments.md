---
title: "Data type(s) of the type parameter(s) in extension method &#39;&lt;methodname&gt;&#39; defined in &#39;&lt;typename&gt;&#39; cannot be inferred from these arguments"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 55274b01-6d78-4950-861e-07d9273ef76e
caps.latest.revision: 7
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Data type(s) of the type parameter(s) in extension method &#39;&lt;methodname&gt;&#39; defined in &#39;&lt;typename&gt;&#39; cannot be inferred from these arguments
Data type(s) of the type parameter(s) in extension method '<methodname\>' defined in '<typename\>' cannot be inferred from these arguments. Specifying the data type(s) explicitly might correct this error.  
  
 An attempt has been made to use type inference to determine the data type (or types) of the type parameter (or parameters) when evaluating a call to a generic extension method. However, the compiler is not able to find a data type for the type parameters in this method, and it reports the error.  
  
> [!NOTE]
>  When specifying arguments is not an option (for example, for query operators in query expressions), the error message appears without the second sentence.  
  
 The following code demonstrates the error.  
  
```vb#  
Module Module1  
  
    Sub Main()  
  
        Dim classInstance As ClassExample  
  
        '' Not valid.  
        'classInstance.GenericExtensionMethod("Hello", "World")  
  
    End Sub  
  
    <System.Runtime.CompilerServices.Extension()> _  
    Sub GenericExtensionMethod(Of T)(ByVal classEx As ClassExample, _  
                                     ByVal x As String, ByVal y As _  
                                     InterfaceExample(Of T))  
    End Sub  
  
End Module  
  
Interface InterfaceExample(Of T)  
End Interface  
  
Class ClassExample  
End Class  
```  
  
 **Error ID:** BC36649 and BC36646  
  
### To correct this error  
  
-   You may be able to specify a data type for the type parameter or parameters instead of relying on type inference.  
  
## See Also  
 [Relaxed Delegate Conversion](../vs140/Relaxed-Delegate-Conversion--Visual-Basic-.md)   
 [Extension Methods (Visual Basic)](../Topic/Extension%20Methods%20\(Visual%20Basic\).md)   
 [Generic Procedures in Visual Basic](../vs140/Generic-Procedures-in-Visual-Basic.md)   
 [Type Conversions in Visual Basic](../vs140/Type-Conversions-in-Visual-Basic.md)