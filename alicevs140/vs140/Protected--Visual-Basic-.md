---
title: "Protected (Visual Basic)"
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
ms.assetid: 74ad3d56-309f-49d2-b60c-1d0157d010e8
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Protected (Visual Basic)
Specifies that one or more declared programming elements are accessible only from within their own class or from a derived class.  
  
## Remarks  
 Sometimes a programming element declared in a class contains sensitive data or restricted code, and you want to limit access to the element. However, if the class is inheritable and you expect a hierarchy of derived classes, it might be necessary for these derived classes to access the data or code. In such a case, you want the element to be accessible both from the base class and from all derived classes. To limit access to an element in this manner, you can declare it with `Protected`.  
  
## Rules  
  
-   **Declaration Context.** You can use `Protected` only at class level. This means the declaration context for a `Protected` element must be a class, and cannot be a source file, namespace, interface, module, structure, or procedure.  
  
-   **Combined Modifiers.** You can use the `Protected` modifier together with the [Friend](../Topic/Friend%20\(Visual%20Basic\).md) modifier in the same declaration. This combination makes the declared elements accessible from anywhere in the same assembly, from their own class, and from derived classes. You can specify `Protected Friend` only on members of classes.  
  
## Behavior  
  
-   **Access Level.** All code in a class can access its elements. Code in any class that derives from a base class can access all the `Protected` elements of the base class. This is true for all generations of derivation. This means that a class can access `Protected` elements of the base class of the base class, and so on.  
  
     Protected access is not a superset or subset of friend access.  
  
-   **Access Modifiers.** The keywords that specify access level are called *access modifiers*. For a comparison of the access modifiers, see [Access Levels in Visual Basic](../vs140/Access-Levels-in-Visual-Basic.md).  
  
 The `Protected` modifier can be used in these contexts:  
  
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
 [Friend](../Topic/Friend%20\(Visual%20Basic\).md)   
 [Private](../vs140/Private--Visual-Basic-.md)   
 [Access Levels in Visual Basic](../vs140/Access-Levels-in-Visual-Basic.md)   
 [Procedures in Visual Basic](../vs140/Procedures-in-Visual-Basic.md)   
 [Structures](../vs140/Structures--Visual-Basic-.md)   
 [Objects and Classes in Visual Basic](../Topic/Objects%20and%20Classes%20in%20Visual%20Basic.md)