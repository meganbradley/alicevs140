---
title: "Property &#39;&lt;propertyname&gt;&#39; doesn&#39;t return a value on all code paths"
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
ms.assetid: 06800966-9c3b-4844-9f13-83ac95607d32
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Property &#39;&lt;propertyname&gt;&#39; doesn&#39;t return a value on all code paths
Property '<propertyname\>' doesn't return a value on all code paths. A null reference exception could occur at run time when the result is used.  
  
 A property `Get` procedure has at least one possible path through its code that does not return a value.  
  
 You can return a value from a property `Get` procedure in any of the following ways:  
  
-   Assign the value to the property name and then perform an `Exit Property` statement.  
  
-   Assign the value to the property name and then perform the `End Get` statement.  
  
-   Include the value in a [Return Statement (Visual Basic)](../vs140/Return-Statement--Visual-Basic-.md).  
  
 If control passes to `Exit Property` or `End Get` and you have not assigned any value to the property name, the `Get` procedure returns the default value of the property's data type. For more information, see "Behavior" in [Function Statement (Visual Basic)](../Topic/Function%20Statement%20\(Visual%20Basic\).md).  
  
 By default, this message is a warning. For more information on hiding warnings or treating warnings as errors, see [Configuring Warnings in Visual Basic](../vs140/Configuring-Warnings-in-Visual-Basic.md).  
  
 **Error ID:** BC42107  
  
### To correct this error  
  
-   Check your control flow logic and make sure you assign a value before every statement that causes a return.  
  
     It is easier to guarantee that every return from the procedure returns a value if you always use the `Return` statement. If you do this, the last statement before `End Get` should be a `Return` statement.  
  
## See Also  
 [Property Procedures](../vs140/Property-Procedures--Visual-Basic-.md)   
 [Property Statement](../vs140/Property-Statement.md)   
 [Get Statement](../vs140/Get-Statement.md)