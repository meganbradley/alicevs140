---
title: "- Operator (Visual Basic)1"
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
H1: - Operator (Visual Basic)
ms.assetid: bff2c368-662d-4c92-ac87-1d9bdfd3426a
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# - Operator (Visual Basic)1
Returns the difference between two numeric expressions or the negative value of a numeric expression.  
  
## Syntax  
  
```  
  
      expression1 – expression2  
- or -  
– expression1  
```  
  
## Parts  
 `expression1`  
 Required. Any numeric expression.  
  
 `expression2`  
 Required unless the `–` operator is calculating a negative value. Any numeric expression.  
  
## Result  
 The result is the difference between `expression1` and `expression2`, or the negated value of `expression1`.  
  
 The result data type is a numeric type appropriate for the data types of `expression1` and `expression2`. See the "Integer Arithmetic" tables in [Data Types of Operator Results](../Topic/Data%20Types%20of%20Operator%20Results%20\(Visual%20Basic\).md).  
  
## Supported Types  
 All numeric types. This includes the unsigned and floating-point types and `Decimal`.  
  
## Remarks  
 In the first usage shown in the syntax shown previously, the `–` operator is the *binary* arithmetic subtraction operator for the difference between two numeric expressions.  
  
 In the second usage shown in the syntax shown previously, the `–` operator is the *unary* negation operator for the negative value of an expression. In this sense, the negation consists of reversing the sign of `expression1` so that the result is positive if `expression1` is negative.  
  
 If either expression evaluates to [Nothing](../Topic/Nothing%20\(Visual%20Basic\).md), the `–` operator treats it as zero.  
  
> [!NOTE]
>  The `–` operator can be *overloaded*, which means that a class or structure can redefine its behavior when an operand has the type of that class or structure. If your code uses this operator on such a class or structure, make sure that you understand its redefined behavior. For more information, see [Operator Procedures](../vs140/Operator-Procedures--Visual-Basic-.md).  
  
## Example  
 The following example uses the `–` operator to calculate and return the difference between two numbers, and then to negate a number.  
  
 [!CODE [VbVbalrOperators#10](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrOperators#10)]  
  
 Following the execution of these statements, `binaryResult` contains 124.45 and `unaryResult` contains –334.90.  
  
## See Also  
 [-= Operator (Visual Basic)](../vs140/-=-Operator--Visual-Basic-2.md)   
 [Arithmetic Operators](../vs140/Arithmetic-Operators--Visual-Basic-.md)   
 [Operator Precedence in Visual Basic](../vs140/Operator-Precedence-in-Visual-Basic.md)   
 [Operators Listed by Functionality](../vs140/Operators-Listed-by-Functionality--Visual-Basic-.md)   
 [Arithmetic Operators in Visual Basic](../Topic/Arithmetic%20Operators%20in%20Visual%20Basic.md)