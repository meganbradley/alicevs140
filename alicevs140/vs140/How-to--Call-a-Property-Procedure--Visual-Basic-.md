---
title: "How to: Call a Property Procedure (Visual Basic)"
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
ms.assetid: 96bc4d74-d9c3-4b7a-954d-58ac8553cd94
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Call a Property Procedure (Visual Basic)
You call a property procedure by storing a value in the property or retrieving its value. You access a property the same way you access a variable.  
  
 The property's `Set` procedure stores a value, and its `Get` procedure retrieves the value. However, you do not explicitly call these procedures by name. You use the property in an assignment statement or an expression, just as you would store or retrieve the value of a variable. [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)] makes the calls to the property's procedures.  
  
### To call a property's Get procedure  
  
1.  Use the property name in an expression the same way you would use a variable name. You can use a property anywhere you can use a variable or a constant.  
  
     -or-  
  
     Use the property name following the equal (`=`) sign in an assignment statement.  
  
     The following example reads the value of the <xref:Microsoft.VisualBasic.DateAndTime.Now?qualifyHint=False> property, implicitly calling its `Get` procedure.  
  
     [!CODE [VbVbalrDateProperties#4](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrDateProperties#4)]  
  
2.  If the property takes arguments, follow the property name with parentheses to enclose the argument list. If there are no arguments, you can optionally omit the parentheses.  
  
3.  Place the arguments in the argument list within the parentheses, separated by commas. Be sure you supply the arguments in the same order that the property defines the corresponding parameters.  
  
 The value of the property participates in the expression just as a variable or constant would, or it is stored in the variable or property on the left side of the assignment statement.  
  
### To call a property's Set procedure  
  
1.  Use the property name on the left side of an assignment statement.  
  
     The following example sets the value of the <xref:Microsoft.VisualBasic.DateAndTime.TimeOfDay?qualifyHint=False> property, implicitly calling the `Set` procedure.  
  
     [!CODE [VbVbcnProcedures#11](../CodeSnippet/VS_Snippets_VBCSharp/VbVbcnProcedures#11)]  
  
2.  If the property takes arguments, follow the property name with parentheses to enclose the argument list. If there are no arguments, you can optionally omit the parentheses.  
  
3.  Place the arguments in the argument list within the parentheses, separated by commas. Be sure you supply the arguments in the same order that the property defines the corresponding parameters.  
  
 The value generated on the right side of the assignment statement is stored in the property.  
  
## See Also  
 [Property Procedures](../vs140/Property-Procedures--Visual-Basic-.md)   
 [Procedure Parameters and Arguments](../vs140/Procedure-Parameters-and-Arguments--Visual-Basic-.md)   
 [Property Statement](../vs140/Property-Statement.md)   
 [Differences Between Properties and Variables in Visual Basic](../vs140/Differences-Between-Properties-and-Variables-in-Visual-Basic.md)   
 [How to: Create a Property](../vs140/How-to--Create-a-Property--Visual-Basic-.md)   
 [How to: Declare a Property with Mixed Access Levels](../vs140/How-to--Declare-a-Property-with-Mixed-Access-Levels--Visual-Basic-.md)   
 [How to: Declare and Call a Default Property in Visual Basic](../Topic/How%20to:%20Declare%20and%20Call%20a%20Default%20Property%20in%20Visual%20Basic.md)   
 [How to: Put a Value in a Property](../Topic/How%20to:%20Put%20a%20Value%20in%20a%20Property%20\(Visual%20Basic\).md)   
 [How to: Get a Value from a Property](../vs140/How-to--Get-a-Value-from-a-Property--Visual-Basic-.md)   
 [Get Statement](../vs140/Get-Statement.md)   
 [Set Statement (Visual Basic)](../vs140/Set-Statement--Visual-Basic-.md)