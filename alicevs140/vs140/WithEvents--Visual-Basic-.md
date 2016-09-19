---
title: "WithEvents (Visual Basic)"
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
ms.assetid: 19d461f5-d72f-4de9-8c1d-0a6650316990
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# WithEvents (Visual Basic)
Specifies that one or more declared member variables refer to an instance of a class that can raise events.  
  
## Remarks  
 When a variable is defined using `WithEvents`, you can declaratively specify that a method handles the variable's events using the `Handles` keyword.  
  
 You can use `WithEvents` only at class or module level. This means the declaration context for a `WithEvents` variable must be a class or module and cannot be a source file, namespace, structure, or procedure.  
  
 You cannot use `WithEvents` on a structure member.  
  
 You can declare only individual variables—not arrays—with `WithEvents`.  
  
## Rules  
  
-   **Element Types.** You must declare `WithEvents` variables to be object variables so that they can accept class instances. However, you cannot declare them as `Object`. You must declare them as the specific class that can raise the events.  
  
 The `WithEvents` modifier can be used in this context: [Dim Statement](../Topic/Dim%20Statement%20\(Visual%20Basic\).md)  
  
## See Also  
 [Handles](../vs140/Handles-Clause--Visual-Basic-.md)   
 [Keywords (Visual Basic)](../vs140/Keywords--Visual-Basic-.md)   
 [Events in Visual Basic](../vs140/Events--Visual-Basic-.md)