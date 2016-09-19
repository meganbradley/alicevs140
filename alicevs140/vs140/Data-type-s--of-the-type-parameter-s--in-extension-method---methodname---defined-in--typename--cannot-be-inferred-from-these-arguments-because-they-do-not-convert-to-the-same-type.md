---
title: "Data type(s) of the type parameter(s) in extension method &#39;&lt;methodname&gt;&#39; defined in &#39;typename&#39; cannot be inferred from these arguments because they do not convert to the same type"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 0bff97fd-cbe9-4433-8192-6498c6fb5d04
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Data type(s) of the type parameter(s) in extension method &#39;&lt;methodname&gt;&#39; defined in &#39;typename&#39; cannot be inferred from these arguments because they do not convert to the same type
Data type(s) of the type parameter(s) in extension method '<methodname\>' defined in 'typename' cannot be inferred from these arguments because they do not convert to the same type. Specifying the data type(s) explicitly might correct this error.  
  
 An attempt has been made to use type inference to determine the data type (or types) of the type parameter (or parameters) when evaluating a call to a generic extension method. The compiler could not find a data type that meets the constraints of all the arguments. Therefore, it reported this error.  
  
> [!NOTE]
>  When specifying arguments is not an option (for example, for query operators in query expressions), the error message appears without the second sentence.  
  
 The following code demonstrates the error.  
  
```vb#  
Option Strict Off  
Module Module3  
    Sub Main()  
  
        Dim c1 As New Class1  
  
        '' Not valid. Integer and Date do not convert to the same type.  
        'c1.targetMethod(19, #3/4/2007#)  
  
    End Sub  
  
    <System.Runtime.CompilerServices.Extension()> _  
    Sub targetMethod(Of T)(ByVal p0 As Class1, ByVal p1 As T, ByVal p2 As T)  
    End Sub  
  
    Class Class1  
    End Class  
  
End Module  
```  
  
 **Error ID:** BC36661 and BC36658  
  
### To correct this error  
  
-   You might be able to convert one or more arguments explicitly to a compatible type, as shown in the following code:  
  
    ```  
    c1.targetMethod(19, #3/4/2007#.ToOADate)  
    ```  
  
-   You might be able to specify a data type for the type parameter or parameters to which the arguments convert, as shown in the following code:  
  
    ```  
    c1.targetMethod(Of String)(19, #3/4/2007#)  
    ```  
  
## See Also  
 [Extension Methods (Visual Basic)](../Topic/Extension%20Methods%20\(Visual%20Basic\).md)   
 [Relaxed Delegate Conversion](../vs140/Relaxed-Delegate-Conversion--Visual-Basic-.md)   
 [Generic Procedures in Visual Basic](../vs140/Generic-Procedures-in-Visual-Basic.md)   
 [Type Conversion Functions](../vs140/Type-Conversion-Functions--Visual-Basic-.md)   
 [Implicit and Explicit Conversions](../Topic/Implicit%20and%20Explicit%20Conversions%20\(Visual%20Basic\).md)   
 [Type Conversions in Visual Basic](../vs140/Type-Conversions-in-Visual-Basic.md)