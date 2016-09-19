---
title: "Other Control Structures (Visual Basic)"
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
ms.assetid: 24b811f7-98ba-40ec-8dd3-4d528cfa4574
caps.latest.revision: 21
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Other Control Structures (Visual Basic)
[!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)] provides control structures that help you dispose of a resource or reduce the number of times you have to repeat an object reference.  
  
## Using...End Using Construction  
 The `Using...End Using` construction establishes a statement block within which you make use of a resource such as a SQL connection. You can optionally acquire the resource with the `Using` statement. When you exit the `Using` block, [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)] automatically disposes of the resource so that it is available for other code to use. The resource must be local and disposable. For more information, see [Using Statement (Visual Basic)](../Topic/Using%20Statement%20\(Visual%20Basic\).md).  
  
## With...End With Construction  
 The `With...End With` construction lets you specify an object reference once and then run a series of statements that access its members. This can simplify your code and improve performance because [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)] does not have to re-establish the reference for each statement that accesses it. For more information, see [With...End With Statement (Visual Basic)](../Topic/With...End%20With%20Statement%20\(Visual%20Basic\).md).  
  
## See Also  
 [Control Flow in Visual Basic](../vs140/Control-Flow-in-Visual-Basic.md)   
 [Decision Structures](../vs140/Decision-Structures--Visual-Basic-.md)   
 [Loop Structures](../vs140/Loop-Structures--Visual-Basic-.md)   
 [Nested Control Structures](../vs140/Nested-Control-Structures--Visual-Basic-.md)   
 [Using Statement (Visual Basic)](../Topic/Using%20Statement%20\(Visual%20Basic\).md)   
 [With...End With Statement (Visual Basic)](../Topic/With...End%20With%20Statement%20\(Visual%20Basic\).md)