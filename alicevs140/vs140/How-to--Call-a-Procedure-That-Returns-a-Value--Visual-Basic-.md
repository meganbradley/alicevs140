---
title: "How to: Call a Procedure That Returns a Value (Visual Basic)"
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
ms.assetid: a445127b-0f5f-465a-98fb-3e514b93d115
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Call a Procedure That Returns a Value (Visual Basic)
A `Function` procedure returns a value to the calling code. You call it by including its name and arguments either on the right side of an assignment statement or in an expression.  
  
### To call a Function procedure within an expression  
  
1.  Use the `Function` procedure name the same way you would use a variable. You can use a `Function` procedure call anywhere you can use a variable or constant in an expression.  
  
2.  Follow the procedure name with parentheses to enclose the argument list. If there are no arguments, you can optionally omit the parentheses. However, using the parentheses makes your code easier to read.  
  
3.  Place the arguments in the argument list within the parentheses, separated by commas. Be sure you supply the arguments in the same order that the `Function` procedure defines the corresponding parameters.  
  
     Alternatively, you can pass one or more arguments by name. For more information, see [Argument Passing by Position and by Name](../vs140/Passing-Arguments-by-Position-and-by-Name--Visual-Basic-.md).  
  
4.  The value returned from the procedure participates in the expression just as the value of a variable or constant would.  
  
### To call a Function procedure in an assignment statement  
  
1.  Use the `Function` procedure name following the equal (`=`) sign in the assignment statement.  
  
2.  Follow the procedure name with parentheses to enclose the argument list. If there are no arguments, you can optionally omit the parentheses. However, using the parentheses makes your code easier to read.  
  
3.  Place the arguments in the argument list within the parentheses, separated by commas. Be sure you supply the arguments in the same order that the `Function` procedure defines the corresponding parameters, unless you are passing them by name.  
  
4.  The value returned from the procedure is stored in the variable or property on the left side of the assignment statement.  
  
## Example  
 The following example calls the [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)] <xref:Microsoft.VisualBasic.Interaction.Environ?qualifyHint=False> to retrieve the value of an operating system environment variable. The first line calls `Environ` within an expression, and the second line calls it in an assignment statement. `Environ` takes the variable name as its sole argument. It returns the variable's value to the calling code.  
  
 [!CODE [VbVbcnProcedures#7](../CodeSnippet/VS_Snippets_VBCSharp/VbVbcnProcedures#7)]  
  
## See Also  
 [Function Procedures](../Topic/Function%20Procedures%20\(Visual%20Basic\).md)   
 [Procedure Parameters and Arguments](../vs140/Procedure-Parameters-and-Arguments--Visual-Basic-.md)   
 [Function Statement (Visual Basic)](../Topic/Function%20Statement%20\(Visual%20Basic\).md)   
 [How to: Create a Procedure that Returns a Value](../vs140/How-to--Create-a-Procedure-that-Returns-a-Value--Visual-Basic-.md)   
 [How to: Return a Value from a Procedure](../vs140/How-to--Return-a-Value-from-a-Procedure--Visual-Basic-.md)   
 [How to: Call a Procedure that Does Not Return a Value](../vs140/How-to--Call-a-Procedure-that-Does-Not-Return-a-Value--Visual-Basic-.md)