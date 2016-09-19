---
title: "Anonymous type member name can be inferred only from a simple or qualified name with no arguments"
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
ms.assetid: e3ba1f33-3a71-4f03-9b04-ed5ec17de17c
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Anonymous type member name can be inferred only from a simple or qualified name with no arguments
You cannot infer an anonymous type member name from a complex expression.  
  
```vb#  
Dim numbers() As Integer = {1, 2, 3, 4, 5}  
' Not valid.  
' Dim instanceName1 = New With {numbers(3)}  
```  
  
 For more information about sources from which anonymous types can and cannot infer member names and types, see [How to: Infer Property Names and Types in Anonymous Type Declarations](../vs140/How-to--Infer-Property-Names-and-Types-in-Anonymous-Type-Declarations--Visual-Basic-.md).  
  
 **Error ID:** BC36556  
  
### To correct this error  
  
-   Assign the expression to a member name, as shown in the following code:  
  
    ```  
    Dim instanceName2 = New With {.number = numbers(3)}  
    ```  
  
## See Also  
 [Anonymous Types](../Topic/Anonymous%20Types%20\(Visual%20Basic\).md)   
 [How to: Infer Property Names and Types in Anonymous Type Declarations](../vs140/How-to--Infer-Property-Names-and-Types-in-Anonymous-Type-Declarations--Visual-Basic-.md)