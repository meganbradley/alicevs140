---
title: "Implements Clause (Visual Basic)"
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
ms.assetid: 5252cdf9-964d-4fc6-af0f-0449b7126b5a
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Implements Clause (Visual Basic)
Indicates that a class or structure member is providing the implementation for a member defined in an interface.  
  
## Remarks  
 The `Implements` keyword is not the same as the [Implements Statement](../vs140/Implements-Statement.md). You use the `Implements` statement to specify that a class or structure implements one or more interfaces, and then for each member you use the `Implements` keyword to specify which interface and which member it implements.  
  
 If a class or structure implements an interface, it must include the `Implements` statement immediately after the [Class Statement (Visual Basic)](../Topic/Class%20Statement%20\(Visual%20Basic\).md) or [Structure Statement](../Topic/Structure%20Statement.md), and it must implement all the members defined by the interface.  
  
## Reimplementation  
 In a derived class, you can reimplement an interface member that the base class has already implemented. This is different from overriding the base class member in the following respects:  
  
-   The base class member does not need to be [Overridable](../vs140/Overridable--Visual-Basic-.md) to be reimplemented.  
  
-   You can reimplement the member with a different name.  
  
 The `Implements` keyword can be used in these contexts:  
  
 [Event Statement](../vs140/Event-Statement.md)  
  
 [Function Statement](../Topic/Function%20Statement%20\(Visual%20Basic\).md)  
  
 [Property Statement](../vs140/Property-Statement.md)  
  
 [Sub Statement](../Topic/Sub%20Statement%20\(Visual%20Basic\).md)  
  
## See Also  
 [Implements Statement](../vs140/Implements-Statement.md)   
 [Interface Statement](../vs140/Interface-Statement--Visual-Basic-.md)   
 [Class Statement](../Topic/Class%20Statement%20\(Visual%20Basic\).md)   
 [Structure Statement](../Topic/Structure%20Statement.md)