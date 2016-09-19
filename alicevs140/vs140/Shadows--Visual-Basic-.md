---
title: "Shadows (Visual Basic)"
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
ms.assetid: 6bf687cd-0544-4797-b51b-911125ec57c6
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Shadows (Visual Basic)
Specifies that a declared programming element redeclares and hides an identically named element, or set of overloaded elements, in a base class.  
  
## Remarks  
 The main purpose of shadowing (which is also known as *hiding by name*) is to preserve the definition of your class members. The base class might undergo a change that creates an element with the same name as one you have already defined. If this happens, the `Shadows` modifier forces references through your class to be resolved to the member you defined, instead of to the new base class element.  
  
 Both shadowing and overriding redefine an inherited element, but there are significant differences between the two approaches. For more information, see [Shadowing in Visual Basic](../vs140/Shadowing-in-Visual-Basic.md).  
  
## Rules  
  
-   **Declaration Context.** You can use `Shadows` only at class level. This means the declaration context for a `Shadows` element must be a class, and cannot be a source file, namespace, interface, module, structure, or procedure.  
  
     You can declare only one shadowing element in a single declaration statement.  
  
-   **Combined Modifiers.** You cannot specify `Shadows` together with `Overloads`, `Overrides`, or `Static` in the same declaration.  
  
-   **Element Types.** You can shadow any kind of declared element with any other kind. If you shadow a property or procedure with another property or procedure, the parameters and the return type do not have to match those in the base class property or procedure.  
  
-   **Accessing.** The shadowed element in the base class is normally unavailable from within the derived class that shadows it. However, the following considerations apply.  
  
    -   If the shadowing element is not accessible from the code referring to it, the reference is resolved to the shadowed element. For example, if a `Private` element shadows a base class element, code that does not have permission to access the `Private` element accesses the base class element instead.  
  
    -   If you shadow an element, you can still access the shadowed element through an object declared with the type of the base class. You can also access it through `MyBase`.  
  
 The `Shadows` modifier can be used in these contexts:  
  
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
 [Shared](../Topic/Shared%20\(Visual%20Basic\).md)   
 [Static](../vs140/Static--Visual-Basic-.md)   
 [Private](../vs140/Private--Visual-Basic-.md)   
 [Me, My, MyBase, and MyClass in Visual Basic](../vs140/Me--My--MyBase--and-MyClass-in-Visual-Basic.md)   
 [Inheritance Basics](../vs140/Inheritance-Basics--Visual-Basic-.md)   
 [MustOverride](../vs140/MustOverride--Visual-Basic-.md)   
 [NotOverridable](../vs140/NotOverridable--Visual-Basic-.md)   
 [Overloads](../vs140/Overloads--Visual-Basic-.md)   
 [Overridable](../vs140/Overridable--Visual-Basic-.md)   
 [Overrides](../vs140/Overrides--Visual-Basic-.md)   
 [Shadowing in Visual Basic](../vs140/Shadowing-in-Visual-Basic.md)