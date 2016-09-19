---
title: "&#39;ParamArray&#39; cannot be applied to the first parameter of an extension method"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 0778a854-246f-4c2b-943d-ea8883b3aa6f
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &#39;ParamArray&#39; cannot be applied to the first parameter of an extension method
'ParamArray' cannot be applied to the first parameter of an extension method. The first parameter specifies which type to extend.  
  
 The first parameter of an extension method specifies the data type that the method extends. Therefore, the first parameter is required and cannot be optional. Because a parameter array is automatically optional, it is not valid as the first argument of an extension method.  
  
> [!NOTE]
>  When the method is executed, the instance of the extended data type that invokes the method becomes the argument for the first parameter of the method. For example, the instance `greeting` in `greeting.Print()` is the argument for the first parameter, `str`, in extension method `Public Sub Print (ByVal str As String)`.  
  
 **Error ID:** BC36554  
  
### To correct this error  
  
-   If the parameter array does not specify the data type you want to extend, add a new first parameter that specifies this type.  
  
    ```  
    <Extension()>  
    Public Sub AddTo(ByRef str As String, ByVal ParamArray addOns() As String)  
    ' Concatenate the strings in addOns to str.  
    End Sub  
    ```  
  
-   If the parameter array does specify the data type you want to extend, consider changing it to a regular array, requiring an argument, instead of a parameter array. Regular arrays can be extended.  
  
    ```  
    <Extension()>  
    Public Function Sum(ByVal ints() As Integer) As Integer  
        Dim total As Integer = 0  
        For Each i As Integer In ints  
            total = total + i  
        Next i  
        Return total  
    End Function  
    ```  
  
## See Also  
 [Extension Methods (Visual Basic)](../Topic/Extension%20Methods%20\(Visual%20Basic\).md)   
 [Parameter Arrays](../Topic/Parameter%20Arrays%20\(Visual%20Basic\).md)   
 [Optional Parameters](../vs140/Optional-Parameters--Visual-Basic-.md)