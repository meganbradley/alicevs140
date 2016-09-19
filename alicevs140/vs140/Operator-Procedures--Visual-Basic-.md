---
title: "Operator Procedures (Visual Basic)"
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
ms.assetid: 8c513d38-246b-4fb7-8b75-29e1364e555b
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Operator Procedures (Visual Basic)
An operator procedure is a series of [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)] statements that define the behavior of a standard operator (such as `*`, `<>`, or `And`) on a class or structure you have defined. This is also called *operator overloading*.  
  
## When to Define Operator Procedures  
 When you have defined a class or structure, you can declare variables to be of the type of that class or structure. Sometimes such a variable needs to participate in an operation as part of an expression. To do this, it must be an operand of an operator.  
  
 [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)] defines operators only on its fundamental data types. You can define the behavior of an operator when one or both of the operands are of the type of your class or structure.  
  
 For more information, see [Operator Statement](../vs140/Operator-Statement.md).  
  
## Types of Operator Procedure  
 An operator procedure can be one of the following types:  
  
-   A definition of a unary operator where the argument is of the type of your class or structure.  
  
-   A definition of a binary operator where at least one of the arguments is of the type of your class or structure.  
  
-   A definition of a conversion operator where the argument is of the type of your class or structure.  
  
-   A definition of a conversion operator that returns the type of your class or structure.  
  
 Conversion operators are always unary, and you always use `CType` as the operator you are defining.  
  
## Declaration Syntax  
 The syntax for declaring an operator procedure is as follows:  
  
 `Public Shared`   `[Widening | Narrowing]`   `Operator`  *operatorsymbol*  `(` *operand1*  `[,`  *operand2* `]) As`  *datatype*  
  
 `' Statements of the operator procedure.`  
  
 `End Operator`  
  
 You use the `Widening` or `Narrowing` keyword only on a type conversion operator. The operator symbol is always [CType Function](../Topic/CType%20Function%20\(Visual%20Basic\).md) for a type conversion operator.  
  
 You declare two operands to define a binary operator, and you declare one operand to define a unary operator, including a type conversion operator. All operands must be declared `ByVal`.  
  
 You declare each operand the same way you declare parameters for [Sub Procedures](../vs140/Sub-Procedures--Visual-Basic-.md).  
  
### Data Type  
 Because you are defining an operator on a class or structure you have defined, at least one of the operands must be of the data type of that class or structure. For a type conversion operator, either the operand or the return type must be of the data type of the class or structure.  
  
 For more details, see [Operator Statement](../vs140/Operator-Statement.md).  
  
## Calling Syntax  
 You invoke an operator procedure implicitly by using the operator symbol in an expression. You supply the operands the same way you do for predefined operators.  
  
 The syntax for an implicit call to an operator procedure is as follows:  
  
 `Dim testStruct As`  *structurename*  
  
 `Dim testNewStruct As`  *structurename*  `= testStruct`  *operatorsymbol*  `10`  
  
### Illustration of Declaration and Call  
 The following structure stores a signed 128-bit integer value as the constituent high-order and low-order parts. It defines the `+` operator to add two `veryLong` values and generate a resulting `veryLong` value.  
  
 [!CODE [VbVbcnProcedures#23](../CodeSnippet/VS_Snippets_VBCSharp/VbVbcnProcedures#23)]  
  
 The following example shows a typical call to the `+` operator defined on `veryLong`.  
  
 [!CODE [VbVbcnProcedures#24](../CodeSnippet/VS_Snippets_VBCSharp/VbVbcnProcedures#24)]  
  
 For more information and examples, see [Operator Overloading in Visual Basic 2005](http://go.microsoft.com/fwlink/?LinkId=101703).  
  
## See Also  
 [Procedures in Visual Basic](../vs140/Procedures-in-Visual-Basic.md)   
 [Sub Procedures](../vs140/Sub-Procedures--Visual-Basic-.md)   
 [Function Procedures](../Topic/Function%20Procedures%20\(Visual%20Basic\).md)   
 [Property Procedures](../vs140/Property-Procedures--Visual-Basic-.md)   
 [Procedure Parameters and Arguments](../vs140/Procedure-Parameters-and-Arguments--Visual-Basic-.md)   
 [Operator Statement](../vs140/Operator-Statement.md)   
 [How to: Define an Operator](../vs140/How-to--Define-an-Operator--Visual-Basic-.md)   
 [How to: Define a Conversion Operator](../vs140/How-to--Define-a-Conversion-Operator--Visual-Basic-.md)   
 [How to: Call an Operator Procedure](../Topic/How%20to:%20Call%20an%20Operator%20Procedure%20\(Visual%20Basic\).md)   
 [How to: Consume a Class that Defines Operators](../vs140/How-to--Use-a-Class-that-Defines-Operators--Visual-Basic-.md)