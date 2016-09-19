---
title: "Overrides (Visual Basic)"
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
ms.assetid: 9f5e6144-ce10-465e-842b-1a8f8760af90
caps.latest.revision: 20
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Overrides (Visual Basic)
Specifies that a property or procedure overrides an identically named property or procedure inherited from a base class.  
  
## Remarks  
  
## Rules  
  
-   **Declaration Context.** You can use `Overrides` only in a property or procedure declaration statement.  
  
-   **Combined Modifiers.** You cannot specify `Overrides` together with `Shadows` or `Shared` in the same declaration. Because an overriding element is implicitly overridable, you cannot combine `Overridable` with `Overrides`.  
  
-   **Matching Signatures.** The signature of this declaration must exactly match the *signature* of the property or procedure that it overrides. This means the parameter lists must have the same number of parameters, in the same order, with the same data types.  
  
     In addition to the signature, the overriding declaration must also exactly match the following:  
  
    -   The access level  
  
    -   The return type, if any  
  
-   **Generic Signatures.** For a generic procedure, the signature includes the number of type parameters. Therefore, the overriding declaration must match the base class version in that respect as well.  
  
-   **Additional Matching.** In addition to matching the signature of the base class version, this declaration must also match it in the following respects:  
  
    -   Access-level modifier (such as [Public (Visual Basic)](../vs140/Public--Visual-Basic-.md))  
  
    -   Passing mechanism of each parameter ([ByVal](../vs140/ByVal--Visual-Basic-.md) or [ByRef](../vs140/ByRef--Visual-Basic-.md))  
  
    -   Constraint lists on each type parameter of a generic procedure  
  
-   **Shadowing and Overriding.** Both shadowing and overriding redefine an inherited element, but there are significant differences between the two approaches. For more information, see [Shadowing in Visual Basic](../vs140/Shadowing-in-Visual-Basic.md).  
  
 If you use `Overrides`, the compiler implicitly adds `Overloads` so that your library APIs work with C# more easily.  
  
 The `Overrides` modifier can be used in these contexts:  
  
 [Function Statement](../Topic/Function%20Statement%20\(Visual%20Basic\).md)  
  
 [Property Statement](../vs140/Property-Statement.md)  
  
 [Sub Statement](../Topic/Sub%20Statement%20\(Visual%20Basic\).md)  
  
## See Also  
 [MustOverride](../vs140/MustOverride--Visual-Basic-.md)   
 [NotOverridable](../vs140/NotOverridable--Visual-Basic-.md)   
 [Overridable](../vs140/Overridable--Visual-Basic-.md)   
 [Keywords (Visual Basic)](../vs140/Keywords--Visual-Basic-.md)   
 [Shadowing in Visual Basic](../vs140/Shadowing-in-Visual-Basic.md)   
 [Generic Types in Visual Basic](../Topic/Generic%20Types%20in%20Visual%20Basic%20\(Visual%20Basic\).md)   
 [Type List](../vs140/Type-List--Visual-Basic-.md)