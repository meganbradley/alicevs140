---
title: "How to: Create a Procedure (Visual Basic)"
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
ms.assetid: 4f779247-0b50-47e8-9e5c-ab5cf39ac0d2
caps.latest.revision: 29
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Create a Procedure (Visual Basic)
You enclose a procedure between a starting declaration statement (`Sub` or `Function`) and an ending declaration statement (`End Sub` or `End Function`). All the procedure's code lies between these statements.  
  
 A procedure cannot contain another procedure, so its starting and ending statements must be outside any other procedure.  
  
 If you have code that performs the same task in different places, you can write the task once as a procedure and then call it from different places in your code.  
  
### To create a procedure that does not return a value  
  
1.  Outside any other procedure, use a `Sub` statement, followed by an `End Sub` statement.  
  
2.  In the `Sub` statement, follow the `Sub` keyword with the name of the procedure, then the parameter list in parentheses.  
  
3.  Place the procedure's code statements between the `Sub` and `End Sub` statements.  
  
### To create a procedure that returns a value  
  
1.  Outside any other procedure, use a `Function` statement, followed by an `End Function` statement.  
  
2.  In the `Function` statement, follow the `Function` keyword with the name of the procedure, then the parameter list in parentheses, and then an `As` clause specifying the data type of the return value.  
  
3.  Place the procedure's code statements between the `Function` and `End Function` statements.  
  
4.  Use a `Return` statement to return the value to the calling code.  
  
### To connect your new procedure with the old, repetitive blocks of code  
  
1.  Make sure you define the new procedure in a place where the old code has access to it.  
  
2.  In your old, repetitive code block, replace the statements that perform the repetitive task with a single statement that calls the `Sub` or `Function` procedure.  
  
3.  If your procedure is a `Function` that returns a value, ensure that your calling statement performs an action with the returned value, such as storing it in a variable, or else the value will be lost.  
  
## Example  
 The following `Function` procedure calculates the longest side, or hypotenuse, of a right triangle, given the values for the other two sides.  
  
 [!CODE [VbVbcnProcedures#1](../CodeSnippet/VS_Snippets_VBCSharp/VbVbcnProcedures#1)]  
  
## See Also  
 [Procedures in Visual Basic](../vs140/Procedures-in-Visual-Basic.md)   
 [Sub Procedures](../vs140/Sub-Procedures--Visual-Basic-.md)   
 [Function Procedures](../Topic/Function%20Procedures%20\(Visual%20Basic\).md)   
 [Property Procedures](../vs140/Property-Procedures--Visual-Basic-.md)   
 [Operator Procedures](../vs140/Operator-Procedures--Visual-Basic-.md)   
 [Procedure Parameters and Arguments](../vs140/Procedure-Parameters-and-Arguments--Visual-Basic-.md)   
 [Recursive Procedures](../Topic/Recursive%20Procedures%20\(Visual%20Basic\).md)   
 [Procedure Overloading](../Topic/Procedure%20Overloading%20\(Visual%20Basic\).md)   
 [Objects and Classes in Visual Basic](../Topic/Objects%20and%20Classes%20in%20Visual%20Basic.md)   
 [Object-Oriented Programming with Managed Languages](../vs140/Object-Oriented-Programming--C#-and-Visual-Basic-.md)