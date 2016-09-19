---
title: "MustOverride (Visual Basic)"
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
ms.assetid: 6e9d9ad6-bb64-433f-b32b-3ef84293bf96
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# MustOverride (Visual Basic)
Specifies that a property or procedure is not implemented in this class and must be overridden in a derived class before it can be used.  
  
## Remarks  
 You can use `MustOverride` only in a property or procedure declaration statement. The property or procedure that specifies `MustOverride` must be a member of a class, and the class must be marked [MustInherit](../Topic/MustInherit%20\(Visual%20Basic\).md).  
  
## Rules  
  
-   **Incomplete Declaration.** When you specify `MustOverride`, you do not supply any additional lines of code for the property or procedure, not even the `End Function`, `End Property`, or `End Sub` statement.  
  
-   **Combined Modifiers.** You cannot specify `MustOverride` together with `NotOverridable`, `Overridable`, or `Shared` in the same declaration.  
  
-   **Shadowing and Overriding.** Both shadowing and overriding redefine an inherited element, but there are significant differences between the two approaches. For more information, see [Shadowing in Visual Basic](../vs140/Shadowing-in-Visual-Basic.md).  
  
-   **Alternate Terms.** An element that cannot be used except in an override is sometimes called a *pure virtual* element.  
  
 The `MustOverride` modifier can be used in these contexts:  
  
 [Function Statement](../Topic/Function%20Statement%20\(Visual%20Basic\).md)  
  
 [Property Statement](../vs140/Property-Statement.md)  
  
 [Sub Statement](../Topic/Sub%20Statement%20\(Visual%20Basic\).md)  
  
## See Also  
 [NotOverridable](../vs140/NotOverridable--Visual-Basic-.md)   
 [Overridable](../vs140/Overridable--Visual-Basic-.md)   
 [Overrides](../vs140/Overrides--Visual-Basic-.md)   
 [MustInherit](../Topic/MustInherit%20\(Visual%20Basic\).md)   
 [Keywords (Visual Basic)](../vs140/Keywords--Visual-Basic-.md)   
 [Shadowing in Visual Basic](../vs140/Shadowing-in-Visual-Basic.md)