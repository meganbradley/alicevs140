---
title: "How to: Create a Property (Visual Basic)"
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
ms.assetid: 4d229712-6be8-4c5c-bac5-06995ce9185a
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Create a Property (Visual Basic)
You enclose a property definition between a `Property` statement and an `End Property` statement. Within this definition you define a `Get` procedure, a `Set` procedure, or both. All the property's code lies within these procedures.  
  
 The `Get` procedure retrieves the property's value, and the `Set` procedure stores a value. If you want the property to have read/write access, you must define both procedures. For a read-only property, you define only `Get`, and for a write-only property, you define only `Set`.  
  
### To create a property  
  
1.  Outside any property or procedure, use a [Property Statement](../vs140/Property-Statement.md), followed by an `End Property` statement.  
  
2.  If the property takes parameters, follow the `Property` keyword with the name of the procedure, then the parameter list in parentheses.  
  
3.  Follow the parentheses with an `As` clause to specify the data type of the property's value. You must specify the data type even for a write-only property.  
  
4.  Add `Get` and `Set` procedures, as appropriate. See the following directions.  
  
### To create a Get procedure that retrieves a property value  
  
1.  Between the `Property` and `End Property` statements, write a [Get Statement](../vs140/Get-Statement.md), followed by an `End Get` statement. You do not need to define any parameters for the `Get` procedure.  
  
2.  Place the code statements to retrieve the property's value between the `Get` and `End Get` statements. This code can include other calculations and data manipulations in addition to generating and returning the property's value.  
  
3.  Use a `Return` statement to return the property's value to the calling code.  
  
 You must write a `Get` procedure for a read-write property and for a read-only property. You must not define a `Get` procedure for a write-only property.  
  
### To create a Set procedure that writes a property's value  
  
1.  Between the `Property` and `End Property` statements, write a [Set Statement (Visual Basic)](../vs140/Set-Statement--Visual-Basic-.md), followed by an `End Set` statement.  
  
2.  In the `Set` statement, follow the `Set` keyword with a parameter list in parentheses. This parameter list must include at least a value parameter for the value passed by the calling code. The default name for this value parameter is `Value`, but you can use a different name if appropriate. The value parameter must have the same data type as the property itself.  
  
3.  Place the code statements to store a value in the property between the `Set` and `End Set` statements. This code can include other calculations and data manipulations in addition to validating and storing the property's value.  
  
4.  Use the value parameter to accept the value supplied by the calling code. You can either store this value directly in an assignment statement, or use it in an expression to calculate the internal value to be stored.  
  
 You must write a `Set` procedure for a read-write property and for a write-only property. You must not define a `Set` procedure for a read-only property.  
  
## Example  
 The following example creates a read/write property that stores a full name as two constituent names, the first name and the last name. When the calling code reads `fullName`, the `Get` procedure combines the two constituent names and returns the full name. When the calling code assigns a new full name, the `Set` procedure attempts to break it into two constituent names. If it does not find a space, it stores it all as the first name.  
  
 [!CODE [VbVbcnProcedures#8](../CodeSnippet/VS_Snippets_VBCSharp/VbVbcnProcedures#8)]  
  
 The following example shows typical calls to the property procedures of `fullName`. The first call sets the property value and the second call retrieves it.  
  
 [!CODE [VbVbcnProcedures#9](../CodeSnippet/VS_Snippets_VBCSharp/VbVbcnProcedures#9)]  
  
## See Also  
 [Procedures in Visual Basic](../vs140/Procedures-in-Visual-Basic.md)   
 [Property Procedures](../vs140/Property-Procedures--Visual-Basic-.md)   
 [Procedure Parameters and Arguments](../vs140/Procedure-Parameters-and-Arguments--Visual-Basic-.md)   
 [Differences Between Properties and Variables in Visual Basic](../vs140/Differences-Between-Properties-and-Variables-in-Visual-Basic.md)   
 [How to: Declare a Property with Mixed Access Levels](../vs140/How-to--Declare-a-Property-with-Mixed-Access-Levels--Visual-Basic-.md)   
 [How to: Call a Property Procedure](../vs140/How-to--Call-a-Property-Procedure--Visual-Basic-.md)   
 [How to: Declare and Call a Default Property in Visual Basic](../Topic/How%20to:%20Declare%20and%20Call%20a%20Default%20Property%20in%20Visual%20Basic.md)   
 [How to: Put a Value in a Property](../Topic/How%20to:%20Put%20a%20Value%20in%20a%20Property%20\(Visual%20Basic\).md)   
 [How to: Get a Value from a Property](../vs140/How-to--Get-a-Value-from-a-Property--Visual-Basic-.md)