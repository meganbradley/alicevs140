---
title: "Cannot infer a common type for the first and second operands of the binary &#39;If&#39; operator"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: f46873aa-f6cd-4cc9-9e8e-e668bddf0980
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Cannot infer a common type for the first and second operands of the binary &#39;If&#39; operator
Cannot infer a common type for the first and second operands of the binary 'If' operator. One must have a widening conversion to the other.  
  
 The binary `If` operator requires that there be a widening conversion between one of the arguments and the other argument. For example, because there is not a widening conversion in either direction between `Integer` and `String`, the following code causes this error.  
  
```vb#  
Dim first? As Integer  
Dim second As String = "First is Nothing"  
'' Not valid.  
' Console.WriteLine(If(first, second))  
```  
  
 **Error ID:** BC33110  
  
### To correct this error  
  
-   Provide an explicit conversion for one of the operands, if that is possible in your code:  
  
    ```  
    Console.WriteLine(If(first, CInt(second)))   
    ```  
  
-   Rewrite the code by using a different conditional construction.  
  
    ```  
    If first IsNot Nothing Then  
        Console.WriteLine(first)  
    Else  
        Console.WriteLine(second)  
    End If  
    ```  
  
## See Also  
 [If Operator](../vs140/If-Operator--Visual-Basic-.md)   
 [Widening and Narrowing Conversions](../Topic/Widening%20and%20Narrowing%20Conversions%20\(Visual%20Basic\).md)   
 [If...Then...Else Statement (Visual Basic)](../Topic/If...Then...Else%20Statement%20\(Visual%20Basic\).md)