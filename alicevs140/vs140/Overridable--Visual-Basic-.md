---
title: "Overridable (Visual Basic)"
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
ms.assetid: 612581e7-8a4c-4a5d-beff-3402fffa6f35
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Overridable (Visual Basic)
Specifies that a property or procedure can be overridden by an identically named property or procedure in a derived class.  
  
## Remarks  
 The `Overridable` modifier allows a property or method in a class to be overridden in a derived class. The [NotOverridable (Visual Basic)](../vs140/NotOverridable--Visual-Basic-.md) modifier prevents a property or method from being overridden in a derived class.  For more information, see [Inheritance Basics (Visual Basic)](../vs140/Inheritance-Basics--Visual-Basic-.md).  
  
 If the `Overridable` or `NotOverridable` modifier is not specified, the default setting depends on whether the property or method overrides a base class property or method. If the property or method overrides a base class property or method, the default setting is `Overridable`; otherwise, it is `NotOverridable`.  
  
 You can shadow or override to redefine an inherited element, but there are significant differences between the two approaches. For more information, see [Shadowing in Visual Basic](../vs140/Shadowing-in-Visual-Basic.md).  
  
 An element that can be overridden is sometimes referred to as a *virtual* element. If it can be overridden, but does not have to be, it is sometimes also called a *concrete* element.  
  
 You can use `Overridable` only in a property or procedure declaration statement.  
  
## Combined Modifiers  
 You cannot specify `Overridable` or `NotOverridable` for a `Private` method.  
  
 You cannot specify `Overridable` together with `MustOverride`, `NotOverridable`, or `Shared` in the same declaration.  
  
 Because an overriding element is implicitly overridable, you cannot combine `Overridable` with `Overrides`.  
  
## Usage  
 The `Overridable` modifier can be used in these contexts:  
  
 [Function Statement](../Topic/Function%20Statement%20\(Visual%20Basic\).md)  
  
 [Property Statement](../vs140/Property-Statement.md)  
  
 [Sub Statement](../Topic/Sub%20Statement%20\(Visual%20Basic\).md)  
  
## See Also  
 [Modifiers (Visual Basic)](../vs140/Modifiers--Visual-Basic-.md)   
 [Inheritance Basics (Visual Basic)](../vs140/Inheritance-Basics--Visual-Basic-.md)   
 [MustOverride](../vs140/MustOverride--Visual-Basic-.md)   
 [NotOverridable](../vs140/NotOverridable--Visual-Basic-.md)   
 [Overrides](../vs140/Overrides--Visual-Basic-.md)   
 [Keywords (Visual Basic)](../vs140/Keywords--Visual-Basic-.md)   
 [Shadowing in Visual Basic](../vs140/Shadowing-in-Visual-Basic.md)