---
title: "Data type(s) of the type parameter(s) in method &#39;&lt;methodname&gt;&#39; cannot be inferred from these arguments because they do not convert to the same type"
ms.custom: na
ms.date: 09/18/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: e80c5afd-e16d-4f03-bdf1-c79c4286114b
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Data type(s) of the type parameter(s) in method &#39;&lt;methodname&gt;&#39; cannot be inferred from these arguments because they do not convert to the same type
Data type(s) of the type parameter(s) in method '<methodname\>' cannot be inferred from these arguments because they do not convert to the same type. Specifying the data type(s) explicitly might correct this error.  
  
 An attempt has been made to use type inference to determine the data type or types of the type parameter or parameters when evaluating a call to a generic procedure. The compiler could not find a data type that meets the constraints of all the arguments. Therefore, it reported this error.  
  
> [!NOTE]
>  When specifying arguments is not an option (for example, for query operators in query expressions), the error message appears without the second sentence.  
  
 The following code demonstrates the error.  
  
```vb#  
Option Strict Off  
Module Module1  
    Sub Main()  
  
        '' Not valid. Integer and Date do not convert to the same type.  
        'targetMethod(19, #3/4/2007#)  
  
    End Sub  
  
    Sub targetMethod(Of T)(ByVal p1 As T, ByVal p2 As T)  
    End Sub  
  
End Module  
```  
  
 **Error ID:** BC36660 and BC36657  
  
### To correct this error  
  
-   You may be able to convert one or more arguments explicitly to a compatible type, as shown in the following code:  
  
    ```  
    targetMethod(19, #3/4/2007#.ToOADate)  
    ```  
  
-   You may be able to specify a data type for the type parameter or parameters to which the arguments convert, as shown in the following code:  
  
    ```  
    targetMethod(Of String)(19, #3/4/2007#)  
    ```  
  
## See Also  
 [Generic Procedures in Visual Basic](../vs140/Generic-Procedures-in-Visual-Basic.md)   
 [Type Conversion Functions](../vs140/Type-Conversion-Functions--Visual-Basic-.md)   
 [Implicit and Explicit Conversions](../Topic/Implicit%20and%20Explicit%20Conversions%20\(Visual%20Basic\).md)   
 [Type Conversions in Visual Basic](../vs140/Type-Conversions-in-Visual-Basic.md)