---
title: "Cannot convert anonymous type to expression tree because it contains a field that is used in the initialization of another field"
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
ms.assetid: 27de068f-080e-4160-86bf-1ec23fd1925a
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Cannot convert anonymous type to expression tree because it contains a field that is used in the initialization of another field
The compiler does not accept conversion of an anonymous to an expression tree when one property of the anonymous type is used to initialize another property of the anonymous type. For example, in the following code, `Prop1` is declared in the initialization list and then used as the initial value for `Prop2`.  
  
```vb#  
Module M2  
  
    Sub ExpressionExample(Of T)(ByVal x As Expressions.Expression(Of Func(Of T)))  
    End Sub  
  
    Sub Main()  
        ' The following line causes the error.  
        ' ExpressionExample(Function() New With {.Prop1 = 2, .Prop2 = .Prop1})  
  
    End Sub  
End Module  
```  
  
 **Error ID:** BC36548  
  
### To correct this error  
  
-   Assign the initial value for `Prop1` to a local variable. Assign that variable to both `Prop1` and `Prop2`, as shown in the following code.  
  
    ```  
    Sub Main()  
  
        Dim temp = 2  
        ExpressionExample(Function() New With {.Prop1 = temp, .Prop2 = temp})  
  
    End Sub  
    ```  
  
## See Also  
 [Anonymous Types](../Topic/Anonymous%20Types%20\(Visual%20Basic\).md)   
 [Expression Trees (C# and Visual Basic)](../vs140/Expression-Trees--C#-and-Visual-Basic-.md)   
 [How to: Use Expression Trees to Build Dynamic Queries](../vs140/How-to--Use-Expression-Trees-to-Build-Dynamic-Queries--C#-and-Visual-Basic-.md)