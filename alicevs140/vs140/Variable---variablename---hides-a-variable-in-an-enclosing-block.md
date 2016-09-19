---
title: "Variable &#39;&lt;variablename&gt;&#39; hides a variable in an enclosing block"
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
ms.assetid: e7658ebc-da45-451b-a409-a0f8915f0beb
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Variable &#39;&lt;variablename&gt;&#39; hides a variable in an enclosing block
A variable enclosed in a block has the same name as another local variable.  
  
 **Error ID:** BC30616  
  
### To correct this error  
  
-   Rename the variable in the enclosed block so that it is not the same as any other local variables. For example:  
  
    ```  
    Dim a, b, x As Integer  
    If a = b Then  
       Dim y As Integer = 20 ' Uniquely named block variable.  
    End If  
    ```  
  
-   A common cause for this error is the use of `Catch e As Exception` inside an event handler. If this is the case, name the `Catch` block variable `ex` rather than `e`.  
  
-   Another common source of this error is an attempt to access a local variable declared within a `Try` block in a separate `Catch` block. To correct this, declare the variable outside the `Try...Catch...Finally` structure.  
  
## See Also  
 [Try...Catch...Finally Statement](../vs140/Try...Catch...Finally-Statement--Visual-Basic-.md)   
 [Variable Declaration](../Topic/Variable%20Declaration%20in%20Visual%20Basic.md)