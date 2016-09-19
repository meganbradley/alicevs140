---
title: "Public (Visual Basic)"
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
ms.assetid: 284c9e1b-ed23-499b-9bc9-ad87c11485a5
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Public (Visual Basic)
Specifies that one or more declared programming elements have no access restrictions.  
  
## Remarks  
 If you are publishing a component or set of components, such as a class library, you usually want the programming elements to be accessible by any code that interoperates with your assembly. To confer such unlimited access on an element, you can declare it with `Public`.  
  
 Public access is the normal level for a programming element when you do not need to limit access to it. Note that the access level of an element declared within an interface, module, class, or structure defaults to `Public` if you do not declare it otherwise.  
  
## Rules  
  
-   **Declaration Context.** You can use `Public` only at module, interface, or namespace level. This means the declaration context for a `Public` element must be a source file, namespace, interface, module, class, or structure, and cannot be a procedure.  
  
## Behavior  
  
-   **Access Level.** All code that can access a module, class, or structure can access its `Public` elements.  
  
-   **Default Access.** Local variables inside a procedure default to public access, and you cannot use any access modifiers on them.  
  
-   **Access Modifiers.** The keywords that specify access level are called *access modifiers*. For a comparison of the access modifiers, see [Access Levels in Visual Basic](../vs140/Access-Levels-in-Visual-Basic.md).  
  
 The `Public` modifier can be used in these contexts:  
  
 [Class Statement](../Topic/Class%20Statement%20\(Visual%20Basic\).md)  
  
 [Const Statement](../Topic/Const%20Statement%20\(Visual%20Basic\).md)  
  
 [Declare Statement](../Topic/Declare%20Statement.md)  
  
 [Delegate Statement](../vs140/Delegate-Statement.md)  
  
 [Dim Statement](../Topic/Dim%20Statement%20\(Visual%20Basic\).md)  
  
 [Enum Statement](../Topic/Enum%20Statement%20\(Visual%20Basic\).md)  
  
 [Event Statement](../vs140/Event-Statement.md)  
  
 [Function Statement](../Topic/Function%20Statement%20\(Visual%20Basic\).md)  
  
 [Interface Statement](../vs140/Interface-Statement--Visual-Basic-.md)  
  
 [Module Statement](../Topic/Module%20Statement.md)  
  
 [Operator Statement](../vs140/Operator-Statement.md)  
  
 [Property Statement](../vs140/Property-Statement.md)  
  
 [Structure Statement](../Topic/Structure%20Statement.md)  
  
 [Sub Statement](../Topic/Sub%20Statement%20\(Visual%20Basic\).md)  
  
## See Also  
 [Protected](../vs140/Protected--Visual-Basic-.md)   
 [Friend](../Topic/Friend%20\(Visual%20Basic\).md)   
 [Private](../vs140/Private--Visual-Basic-.md)   
 [Access Levels in Visual Basic](../vs140/Access-Levels-in-Visual-Basic.md)   
 [Procedures in Visual Basic](../vs140/Procedures-in-Visual-Basic.md)   
 [Structures](../vs140/Structures--Visual-Basic-.md)   
 [Objects and Classes in Visual Basic](../Topic/Objects%20and%20Classes%20in%20Visual%20Basic.md)