---
title: "How to: Get a Value from a Property (Visual Basic)"
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
ms.assetid: 3954423e-6ab7-4a4c-b55c-a8d27be47891
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Get a Value from a Property (Visual Basic)
You retrieve a property's value by including the property name in an expression.  
  
 The property's `Get` procedure retrieves the value, but you do not explicitly call it by name. You use the property just as you would use a variable. [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)] makes the calls to the property's procedures.  
  
### To retrieve a value from a property  
  
1.  Use the property name in an expression the same way you would use a variable name. You can use a property anywhere you can use a variable or a constant.  
  
     -or-  
  
     Use the property name following the equal (`=`) sign in an assignment statement.  
  
     The following example reads the value of the [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)] `Now` property, implicitly calling its `Get` procedure.  
  
     [!CODE [VbVbalrDateProperties#4](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrDateProperties#4)]  
  
2.  If the property takes arguments, follow the property name with parentheses to enclose the argument list. If there are no arguments, you can optionally omit the parentheses.  
  
3.  Place the arguments in the argument list within the parentheses, separated by commas. Be sure you supply the arguments in the same order that the property defines the corresponding parameters.  
  
 The value of the property participates in the expression just as a variable or constant would, or it is stored in the variable or property on the left side of the assignment statement.  
  
## See Also  
 [Procedures in Visual Basic](../vs140/Procedures-in-Visual-Basic.md)   
 [Property Procedures](../vs140/Property-Procedures--Visual-Basic-.md)   
 [Procedure Parameters and Arguments](../vs140/Procedure-Parameters-and-Arguments--Visual-Basic-.md)   
 [Property Statement](../vs140/Property-Statement.md)   
 [Differences Between Properties and Variables](../vs140/Differences-Between-Properties-and-Variables-in-Visual-Basic.md)   
 [How to: Create a Property](../vs140/How-to--Create-a-Property--Visual-Basic-.md)   
 [How to: Declare a Property with Mixed Access Levels](../vs140/How-to--Declare-a-Property-with-Mixed-Access-Levels--Visual-Basic-.md)   
 [How to: Call a Property Procedure](../vs140/How-to--Call-a-Property-Procedure--Visual-Basic-.md)   
 [How to: Declare and Call a Default Property (Visual Basic)](../Topic/How%20to:%20Declare%20and%20Call%20a%20Default%20Property%20in%20Visual%20Basic.md)   
 [How to: Put a Value in a Property](../Topic/How%20to:%20Put%20a%20Value%20in%20a%20Property%20\(Visual%20Basic\).md)