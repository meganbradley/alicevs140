---
title: "-= Operator (Visual Basic)2"
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
H1: -= Operator (Visual Basic)
ms.assetid: 5ead0c37-ae50-48f7-8435-8e341d81cae1
caps.latest.revision: 21
translation.priority.ht: 
  - de-de
  - ja-jp
---
# -= Operator (Visual Basic)2
Subtracts the value of an expression from the value of a variable or property and assigns the result to the variable or property.  
  
## Syntax  
  
```  
  
variableorproperty -= expression  
```  
  
## Parts  
 `variableorproperty`  
 Required. Any numeric variable or property.  
  
 `expression`  
 Required. Any numeric expression.  
  
## Remarks  
 The element on the left side of the `-=` operator can be a simple scalar variable, a property, or an element of an array. The variable or property cannot be [ReadOnly (Visual Basic)](../vs140/ReadOnly--Visual-Basic-.md).  
  
 The `-=` operator first subtracts the value of the expression (on the right-hand side of the operator) from the value of the variable or property (on the left-hand side of the operator). The operator then assigns the result of that operation to the variable or property.  
  
## Overloading  
 The [- Operator (Visual Basic)](../vs140/--Operator--Visual-Basic-1.md) can be *overloaded*, which means that a class or structure can redefine its behavior when an operand has the type of that class or structure. Overloading the `-` operator affects the behavior of the `-=` operator. If your code uses `-=` on a class or structure that overloads `-`, be sure you understand its redefined behavior. For more information, see [Operator Procedures](../vs140/Operator-Procedures--Visual-Basic-.md).  
  
## Example  
 The following example uses the `-=` operator to subtract one `Integer` variable from another and assign the result to the latter variable.  
  
 [!CODE [VbVbalrOperators#11](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrOperators#11)]  
  
## See Also  
 [- Operator (Visual Basic)](../vs140/--Operator--Visual-Basic-1.md)   
 [Assignment Operators](../vs140/Assignment-Operators--Visual-Basic-.md)   
 [Arithmetic Operators](../vs140/Arithmetic-Operators--Visual-Basic-.md)   
 [Operator Precedence in Visual Basic](../vs140/Operator-Precedence-in-Visual-Basic.md)   
 [Operators Listed by Functionality](../vs140/Operators-Listed-by-Functionality--Visual-Basic-.md)   
 [Statements in Visual Basic](../vs140/Statements-in-Visual-Basic.md)