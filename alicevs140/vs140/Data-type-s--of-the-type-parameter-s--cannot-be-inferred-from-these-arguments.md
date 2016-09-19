---
title: "Data type(s) of the type parameter(s) cannot be inferred from these arguments"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - VB
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-visual-basic
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 0e0050f2-2039-4311-b260-f0ebfde84189
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Data type(s) of the type parameter(s) cannot be inferred from these arguments
Data type(s) of the type parameter(s) cannot be inferred from these arguments. Specifying the data type(s) explicitly might correct this error.  
  
 This error occurs when overload resolution has failed. It occurs as a subordinate message that states why a particular overload candidate has been eliminated. The error message explains that the compiler cannot use type inference to find data types for the type parameters.  
  
> [!NOTE]
>  When specifying arguments is not an option (for example, for query operators in query expressions), the error message appears without the second sentence.  
  
 The following code demonstrates the error.  
  
```vb#  
Module Module1  
  
    Sub Main()  
  
        '' Not Valid.  
        'OverloadedGenericMethod("Hello", "World")  
  
    End Sub  
  
    Sub OverloadedGenericMethod(Of T)(ByVal x As String,   
                                      ByVal y As InterfaceExample(Of T))  
    End Sub  
  
    Sub OverloadedGenericMethod(Of T, R)(ByVal x As T,   
                                         ByVal y As InterfaceExample(Of R))  
    End Sub  
  
End Module  
  
Interface InterfaceExample(Of T)  
End Interface  
```  
  
 **Error ID:** BC36647 and BC36644  
  
### To correct this error  
  
-   You may be able to specify a data type for the type parameter or parameters instead of relying on type inference.  
  
## See Also  
 [Relaxed Delegate Conversion](../vs140/Relaxed-Delegate-Conversion--Visual-Basic-.md)   
 [Generic Procedures in Visual Basic](../vs140/Generic-Procedures-in-Visual-Basic.md)   
 [Type Conversions in Visual Basic](../vs140/Type-Conversions-in-Visual-Basic.md)