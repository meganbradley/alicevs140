---
title: "Private (Visual Basic)"
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
ms.assetid: aba74a2e-5824-4613-bf63-b9ec7787f4e6
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Private (Visual Basic)
Specifies that one or more declared programming elements are accessible only from within their declaration context, including from within any contained types.  
  
## Remarks  
 If a programming element represents proprietary functionality, or contains confidential data, you usually want to limit access to it as strictly as possible. You achieve the maximum limitation by allowing only the module, class, or structure that defines it to access it. To limit access to an element in this way, you can declare it with `Private`.  
  
## Rules  
  
-   **Declaration Context.** You can use `Private` only at module level. This means the declaration context for a `Private` element must be a module, class, or structure, and cannot be a source file, namespace, interface, or procedure.  
  
## Behavior  
  
-   **Access Level.** All code within a declaration context can access its `Private` elements. This includes code within a contained type, such as a nested class or an assignment expression in an enumeration. No code outside of the declaration context can access its `Private` elements.  
  
-   **Access Modifiers.** The keywords that specify access level are called *access modifiers*. For a comparison of the access modifiers, see [Access Levels in Visual Basic](../vs140/Access-Levels-in-Visual-Basic.md).  
  
 The `Private` modifier can be used in these contexts:  
  
 [Class Statement](../Topic/Class%20Statement%20\(Visual%20Basic\).md)  
  
 [Const Statement](../Topic/Const%20Statement%20\(Visual%20Basic\).md)  
  
 [Declare Statement](../Topic/Declare%20Statement.md)  
  
 [Delegate Statement](../vs140/Delegate-Statement.md)  
  
 [Dim Statement](../Topic/Dim%20Statement%20\(Visual%20Basic\).md)  
  
 [Enum Statement](../Topic/Enum%20Statement%20\(Visual%20Basic\).md)  
  
 [Event Statement](../vs140/Event-Statement.md)  
  
 [Function Statement](../Topic/Function%20Statement%20\(Visual%20Basic\).md)  
  
 [Interface Statement](../vs140/Interface-Statement--Visual-Basic-.md)  
  
 [Property Statement](../vs140/Property-Statement.md)  
  
 [Structure Statement](../Topic/Structure%20Statement.md)  
  
 [Sub Statement](../Topic/Sub%20Statement%20\(Visual%20Basic\).md)  
  
## See Also  
 [Public](../vs140/Public--Visual-Basic-.md)   
 [Protected](../vs140/Protected--Visual-Basic-.md)   
 [Friend](../Topic/Friend%20\(Visual%20Basic\).md)   
 [Access Levels in Visual Basic](../vs140/Access-Levels-in-Visual-Basic.md)   
 [Procedures in Visual Basic](../vs140/Procedures-in-Visual-Basic.md)   
 [Structures](../vs140/Structures--Visual-Basic-.md)   
 [Objects and Classes in Visual Basic](../Topic/Objects%20and%20Classes%20in%20Visual%20Basic.md)