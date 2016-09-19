---
title: "&#39;Set&#39; accessor of property &#39;&lt;propertyname&gt;&#39; is not accessible"
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
ms.assetid: 6f7b31b7-3656-4ae1-8851-90f5f4c6950a
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &#39;Set&#39; accessor of property &#39;&lt;propertyname&gt;&#39; is not accessible
A statement attempts to store the value of a property when it does not have access to the property's `Set` procedure.  
  
 If the [Set Statement (Visual Basic)](../vs140/Set-Statement--Visual-Basic-.md) is marked with a more restrictive access level than its [Property Statement](../vs140/Property-Statement.md), an attempt to set the property value could fail in the following cases:  
  
-   The `Set` statement is marked [Private (Visual Basic)](../vs140/Private--Visual-Basic-.md) and the calling code is outside the class or structure in which the property is defined.  
  
-   The `Set` statement is marked [Protected (Visual Basic)](../vs140/Protected--Visual-Basic-.md) and the calling code is not in the class or structure in which the property is defined, nor in a derived class.  
  
-   The `Set` statement is marked [Friend (Visual Basic)](../Topic/Friend%20\(Visual%20Basic\).md) and the calling code is not in the same assembly in which the property is defined.  
  
 **Error ID:** BC31102  
  
### To correct this error  
  
-   If you have control of the source code defining the property, consider declaring the `Set` procedure with the same access level as the property itself.  
  
-   If you do not have control of the source code defining the property, or you must restrict the `Set` procedure access level more than the property itself, try to move the statement that sets the property value to a region of code that has better access to the property.  
  
## See Also  
 [Property Procedures](../vs140/Property-Procedures--Visual-Basic-.md)   
 [How to: Declare a Property with Mixed Access Levels](../vs140/How-to--Declare-a-Property-with-Mixed-Access-Levels--Visual-Basic-.md)