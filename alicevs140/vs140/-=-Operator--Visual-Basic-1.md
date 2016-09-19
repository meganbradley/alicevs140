---
title: "-= Operator (Visual Basic)1"
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
H1: /= Operator (Visual Basic)
ms.assetid: a1e22d0e-8380-4761-9da1-84fb51c34821
caps.latest.revision: 25
translation.priority.ht: 
  - de-de
  - ja-jp
---
# -= Operator (Visual Basic)1
Divides the value of a variable or property by the value of an expression and assigns the floating-point result to the variable or property.  
  
## Syntax  
  
```  
  
variableorproperty /= expression  
```  
  
## Parts  
 `variableorproperty`  
 Required. Any numeric variable or property.  
  
 `expression`  
 Required. Any numeric expression.  
  
## Remarks  
 The element on the left side of the `/=` operator can be a simple scalar variable, a property, or an element of an array. The variable or property cannot be [ReadOnly (Visual Basic)](../vs140/ReadOnly--Visual-Basic-.md).  
  
 The `/=` operator first divides the value of the variable or property (on the left-hand side of the operator) by the value of the expression (on the right-hand side of the operator). The operator then assigns the floating-point result of that operation to the variable or property.  
  
 This statement assigns a `Double` value to the variable or property on the left. If `Option Strict` is `On`, `variableorproperty` must be a `Double`. If `Option Strict` is `Off`, Visual Basic performs an implicit conversion and assigns the resulting value to `variableorproperty`, with a possible error at run time. For more information, see [Widening and Narrowing Conversions](../Topic/Widening%20and%20Narrowing%20Conversions%20\(Visual%20Basic\).md) and [Option Strict Statement](../vs140/Option-Strict-Statement.md).  
  
## Overloading  
 The [/ Operator (Visual Basic)](../Topic/-%20Operator%20\(Visual%20Basic\)3.md) can be *overloaded*, which means that a class or structure can redefine its behavior when an operand has the type of that class or structure. Overloading the `/` operator affects the behavior of the `/=` operator. If your code uses `/=` on a class or structure that overloads `/`, be sure you understand its redefined behavior. For more information, see [Operator Procedures](../vs140/Operator-Procedures--Visual-Basic-.md).  
  
## Example  
 The following example uses the `/=` operator to divide one `Integer` variable by a second and assign the quotient to the first variable.  
  
 [!CODE [VbVbalrOperators#17](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrOperators#17)]  
  
## See Also  
 [/ Operator (Visual Basic)](../Topic/-%20Operator%20\(Visual%20Basic\)3.md)   
 [\\= Operator](../vs140/-=-Operator.md)   
 [Assignment Operators](../vs140/Assignment-Operators--Visual-Basic-.md)   
 [Arithmetic Operators](../vs140/Arithmetic-Operators--Visual-Basic-.md)   
 [Operator Precedence in Visual Basic](../vs140/Operator-Precedence-in-Visual-Basic.md)   
 [Operators Listed by Functionality](../vs140/Operators-Listed-by-Functionality--Visual-Basic-.md)   
 [Statements in Visual Basic](../vs140/Statements-in-Visual-Basic.md)