---
title: "How to: Return a Value from a Procedure (Visual Basic)"
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
ms.assetid: 4bcc4724-2b4e-4df8-9b4b-16054607f87d
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Return a Value from a Procedure (Visual Basic)
A `Function` procedure returns a value to the calling code either by executing a `Return` statement or by encountering an `Exit Function` or `End Function` statement.  
  
### To return a value using the Return statement  
  
1.  Put a `Return` statement at the point where the procedure's task is completed.  
  
2.  Follow the `Return` keyword with an expression that yields the value you want to return to the calling code.  
  
3.  You can have more than one `Return` statement in the same procedure.  
  
     The following `Function` procedure calculates the longest side, or hypotenuse, of a right triangle, and returns it to the calling code.  
  
     [!CODE [VbVbcnProcedures#1](../CodeSnippet/VS_Snippets_VBCSharp/VbVbcnProcedures#1)]  
  
     The following example shows a typical call to `hypotenuse`, which stores the returned value.  
  
     [!CODE [VbVbcnProcedures#6](../CodeSnippet/VS_Snippets_VBCSharp/VbVbcnProcedures#6)]  
  
### To return a value using Exit Function or End Function  
  
1.  In at least one place in the `Function` procedure, assign a value to the procedure's name.  
  
2.  When you execute an `Exit Function` or `End Function` statement, [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)] returns the value most recently assigned to the procedure's name.  
  
3.  You can have more than one `Exit Function` statement in the same procedure, and you can mix `Return` and `Exit Function` statements in the same procedure.  
  
4.  You can have only one `End Function` statement in a `Function` procedure.  
  
     For more information and an example, see "Return Value" in [Function Statement (Visual Basic)](../Topic/Function%20Statement%20\(Visual%20Basic\).md).  
  
## See Also  
 [Procedures in Visual Basic](../vs140/Procedures-in-Visual-Basic.md)   
 [Sub Procedures](../vs140/Sub-Procedures--Visual-Basic-.md)   
 [Property Procedures](../vs140/Property-Procedures--Visual-Basic-.md)   
 [Operator Procedures](../vs140/Operator-Procedures--Visual-Basic-.md)   
 [Procedure Parameters and Arguments](../vs140/Procedure-Parameters-and-Arguments--Visual-Basic-.md)   
 [Function Statement](../Topic/Function%20Statement%20\(Visual%20Basic\).md)   
 [Return Statement (Visual Basic)](../vs140/Return-Statement--Visual-Basic-.md)   
 [How to: Create a Procedure that Returns a Value](../vs140/How-to--Create-a-Procedure-that-Returns-a-Value--Visual-Basic-.md)   
 [How to: Call a Procedure that Returns a Value](../vs140/How-to--Call-a-Procedure-That-Returns-a-Value--Visual-Basic-.md)