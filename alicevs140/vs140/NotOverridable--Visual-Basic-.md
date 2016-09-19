---
title: "NotOverridable (Visual Basic)"
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
ms.assetid: 66ec6984-f5f5-4857-b362-6a3907aaf9e0
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# NotOverridable (Visual Basic)
Specifies that a property or procedure cannot be overridden in a derived class.  
  
## Remarks  
 The `NotOverridable` modifier prevents a property or method from being overridden in a derived class.  The [Overridable (Visual Basic)](../vs140/Overridable--Visual-Basic-.md) modifier allows a property or method in a class to be overridden in a derived class. For more information, see [Inheritance Basics (Visual Basic)](../vs140/Inheritance-Basics--Visual-Basic-.md).  
  
 If the `Overridable` or `NotOverridable` modifier is not specified, the default setting depends on whether the property or method overrides a base class property or method. If the property or method overrides a base class property or method, the default setting is `Overridable`; otherwise, it is `NotOverridable`.  
  
 An element that cannot be overridden is sometimes called a *sealed* element.  
  
 You can use `NotOverridable` only in a property or procedure declaration statement. You can specify `NotOverridable` only on a property or procedure that overrides another property or procedure, that is, only in combination with `Overrides`.  
  
## Combined Modifiers  
 You cannot specify `Overridable` or `NotOverridable` for a `Private` method.  
  
 You cannot specify `NotOverridable` together with `MustOverride`, `Overridable`, or `Shared` in the same declaration.  
  
## Usage  
 The `NotOverridable` modifier can be used in these contexts:  
  
 [Function Statement](../Topic/Function%20Statement%20\(Visual%20Basic\).md)  
  
 [Property Statement](../vs140/Property-Statement.md)  
  
 [Sub Statement](../Topic/Sub%20Statement%20\(Visual%20Basic\).md)  
  
## See Also  
 [Modifiers (Visual Basic)](../vs140/Modifiers--Visual-Basic-.md)   
 [Inheritance Basics (Visual Basic)](../vs140/Inheritance-Basics--Visual-Basic-.md)   
 [MustOverride](../vs140/MustOverride--Visual-Basic-.md)   
 [Overridable](../vs140/Overridable--Visual-Basic-.md)   
 [Overrides](../vs140/Overrides--Visual-Basic-.md)   
 [Keywords (Visual Basic)](../vs140/Keywords--Visual-Basic-.md)   
 [Shadowing in Visual Basic](../vs140/Shadowing-in-Visual-Basic.md)