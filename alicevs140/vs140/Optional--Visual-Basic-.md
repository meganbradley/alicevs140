---
title: "Optional (Visual Basic)"
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
ms.assetid: 4571ce88-a539-4115-b230-54eb277c6aa7
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Optional (Visual Basic)
Specifies that a procedure argument can be omitted when the procedure is called.  
  
## Remarks  
 For each optional parameter, you must specify a constant expression as the default value of that parameter. If the expression evaluates to [Nothing](../Topic/Nothing%20\(Visual%20Basic\).md), the default value of the value data type is used as the default value of the parameter.  
  
 If the parameter list contains an optional parameter, every parameter that follows it must also be optional.  
  
 The `Optional` modifier can be used in these contexts:  
  
-   [Declare Statement](../Topic/Declare%20Statement.md)  
  
-   [Function Statement](../Topic/Function%20Statement%20\(Visual%20Basic\).md)  
  
-   [Property Statement](../vs140/Property-Statement.md)  
  
-   [Sub Statement](../Topic/Sub%20Statement%20\(Visual%20Basic\).md)  
  
> [!NOTE]
>  When calling a procedure with or without optional parameters, you can pass arguments by position or by name. For more information, see [Passing Arguments by Position and by Name (Visual Basic)](../vs140/Passing-Arguments-by-Position-and-by-Name--Visual-Basic-.md).  
  
> [!NOTE]
>  You can also define a procedure with optional parameters by using overloading. If you have one optional parameter, you can define two overloaded versions of the procedure, one that accepts the parameter and one that doesn’t. For more information, see [Procedure Overloading (Visual Basic)](../Topic/Procedure%20Overloading%20\(Visual%20Basic\).md).  
  
## Example  
 The following example defines a procedure that has an optional parameter.  
  
```  
Public Function FindMatches(ByRef values As List(Of String),  
                            ByVal searchString As String,  
                            Optional ByVal matchCase As Boolean = False) As List(Of String)  
  
    Dim results As IEnumerable(Of String)  
  
    If matchCase Then  
        results = From v In values  
                  Where v.Contains(searchString)  
    Else  
        results = From v In values  
                  Where UCase(v).Contains(UCase(searchString))  
    End If  
  
    Return results.ToList()  
End Function  
```  
  
## Example  
 The following example demonstrates how to call a procedure with arguments passed by position and with arguments passed by name. The procedure has two optional parameters.  
  
 [!CODE [VbVbalrKeywords#21](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrKeywords#21)]  
  
## See Also  
 [Parameter List (Visual Basic)](../Topic/Parameter%20List%20\(Visual%20Basic\).md)   
 [Optional Parameters (Visual Basic)](../vs140/Optional-Parameters--Visual-Basic-.md)   
 [Keywords (Visual Basic)](../vs140/Keywords--Visual-Basic-.md)