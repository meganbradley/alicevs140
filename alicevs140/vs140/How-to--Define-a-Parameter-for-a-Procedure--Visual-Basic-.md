---
title: "How to: Define a Parameter for a Procedure (Visual Basic)"
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
ms.assetid: 7962808d-407e-4e84-984e-43e9857c53c9
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Define a Parameter for a Procedure (Visual Basic)
A *parameter* allows the calling code to pass a value to the procedure when it calls it. You declare each parameter for a procedure the same way you declare a variable, specifying its name and data type. You also specify the passing mechanism, and whether the parameter is optional.  
  
 For more information, see [Procedure Parameters and Arguments](../vs140/Procedure-Parameters-and-Arguments--Visual-Basic-.md).  
  
### To define a procedure parameter  
  
1.  In the procedure declaration, add the parameter name to the procedure's parameter list, separating it from other parameters by commas.  
  
2.  Decide the data type of the parameter.  
  
3.  Follow the parameter name with an `As` clause to specify the data type.  
  
4.  Decide the passing mechanism you want for the parameter. Normally you pass a parameter by value, unless you want the procedure to be able to change its value in the calling code.  
  
5.  Precede the parameter name with [ByVal](../vs140/ByVal--Visual-Basic-.md) or [ByRef](../vs140/ByRef--Visual-Basic-.md) to specify the passing mechanism. For more information, see [Differences Between Passing an Argument By Value and By Reference](../vs140/Differences-Between-Passing-an-Argument-By-Value-and-By-Reference--Visual-Basic-.md).  
  
6.  If the parameter is optional, precede the passing mechanism with [Optional (Visual Basic)](../vs140/Optional--Visual-Basic-.md) and follow the parameter data type with an equal sign (`=`) and a default value.  
  
     The following example defines the outline of a `Sub` procedure with three parameters. The first two are required and the third is optional. The parameter declarations are separated in the parameter list by commas.  
  
     [!CODE [VbVbcnProcedures#33](../CodeSnippet/VS_Snippets_VBCSharp/VbVbcnProcedures#33)]  
  
     The first parameter accepts a `customer` object, and `updateCustomer` can directly update the variable passed to `c` because the argument is passed [ByRef](../vs140/ByRef--Visual-Basic-.md). The procedure cannot change the values of the last two arguments because they are passed [ByVal](../vs140/ByVal--Visual-Basic-.md).  
  
     If the calling code does not supply a value for the `level` parameter, [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)] sets it to the default value of 0.  
  
     If the type checking switch ([Option Strict Statement](../vs140/Option-Strict-Statement.md)) is `Off`, the `As` clause is optional when you define a parameter. However, if any one parameter uses an `As` clause, all of them must use it. If the type checking switch is `On`, the `As` clause is required for every parameter definition.  
  
     Specifying data types for all your programming elements is known as *strong typing*. When you set `Option Strict On`, [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)] enforces strong typing. This is strongly recommended, for the following reasons:  
  
    -   It enables IntelliSense support for your variables and parameters. This allows you to see their properties and other members as you type in your code.  
  
    -   It allows the compiler to perform type checking. This helps catch statements that can fail at run time due to errors such as overflow. It also catches calls to methods on objects that do not support them.  
  
    -   It results in faster execution of your code. One reason for this is that if you do not specify a data type for a programming element, the [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)] compiler assigns it the `Object` type. Your compiled code might have to convert back and forth between `Object` and other data types, which reduces performance.  
  
## See Also  
 [Procedures in Visual Basic](../vs140/Procedures-in-Visual-Basic.md)   
 [Sub Procedures](../vs140/Sub-Procedures--Visual-Basic-.md)   
 [Function Procedures](../Topic/Function%20Procedures%20\(Visual%20Basic\).md)   
 [How to: Pass Arguments to a Procedure](../Topic/How%20to:%20Pass%20Arguments%20to%20a%20Procedure%20\(Visual%20Basic\).md)   
 [Argument Passing By Value and By Reference](../vs140/Passing-Arguments-by-Value-and-by-Reference--Visual-Basic-.md)   
 [Recursive Procedures](../Topic/Recursive%20Procedures%20\(Visual%20Basic\).md)   
 [Procedure Overloading](../Topic/Procedure%20Overloading%20\(Visual%20Basic\).md)   
 [Objects and Classes in Visual Basic](../Topic/Objects%20and%20Classes%20in%20Visual%20Basic.md)   
 [Object-Oriented Programming with Managed Languages](../vs140/Object-Oriented-Programming--C#-and-Visual-Basic-.md)