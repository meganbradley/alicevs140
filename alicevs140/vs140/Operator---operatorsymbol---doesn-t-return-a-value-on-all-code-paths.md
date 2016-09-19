---
title: "Operator &#39;&lt;operatorsymbol&gt;&#39; doesn&#39;t return a value on all code paths"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 175b2bc9-5233-462d-97de-9d97b003cc46
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Operator &#39;&lt;operatorsymbol&gt;&#39; doesn&#39;t return a value on all code paths
Operator '<operatorsymbol\>' doesn't return a value on all code paths. A null reference exception could occur at run time when the result is used.  
  
 An operator procedure has at least one possible path through its code that does not return a value.  
  
 You can return a value from an operator procedure only by including it in a [Return Statement (Visual Basic)](../vs140/Return-Statement--Visual-Basic-.md).  
  
 If control passes to the `End Operator` statement, the operator procedure returns the default value of the property's data type. For more information, see "Behavior" in [Function Statement (Visual Basic)](../Topic/Function%20Statement%20\(Visual%20Basic\).md).  
  
 By default, this message is a warning. For more information on hiding warnings or treating warnings as errors, see [Configuring Warnings in Visual Basic](../vs140/Configuring-Warnings-in-Visual-Basic.md).  
  
 **Error ID:** BC42106  
  
### To correct this error  
  
-   Check your control flow logic and make sure every possible path ends with a `Return` statement. In particular, the last statement before `End Operator` should be a `Return` statement.  
  
## See Also  
 [Operator Procedures](../vs140/Operator-Procedures--Visual-Basic-.md)   
 [Operator Statement](../vs140/Operator-Statement.md)