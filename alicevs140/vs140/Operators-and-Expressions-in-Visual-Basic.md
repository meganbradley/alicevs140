---
title: "Operators and Expressions in Visual Basic"
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
ms.assetid: b86f3131-94ee-448f-96cd-79611e028b26
caps.latest.revision: 20
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Operators and Expressions in Visual Basic
An *operator* is a code element that performs an operation on one or more code elements that hold values. Value elements include variables, constants, literals, properties, returns from `Function` and `Operator` procedures, and expressions.  
  
 An *expression* is a series of value elements combined with operators, which yields a new value. The operators act on the value elements by performing calculations, comparisons, or other operations.  
  
## Types of Operators  
 [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)] provides the following types of operators:  
  
-   [Arithmetic Operators](../Topic/Arithmetic%20Operators%20in%20Visual%20Basic.md) perform familiar calculations on numeric values, including shifting their bit patterns.  
  
-   [Comparison Operators](../vs140/Comparison-Operators-in-Visual-Basic.md) compare two expressions and return a `Boolean` value representing the result of the comparison.  
  
-   [Concatenation Operators](../Topic/Concatenation%20Operators%20in%20Visual%20Basic.md) join multiple strings into a single string.  
  
-   [Logical and Bitwise Operators in Visual Basic](../vs140/Logical-and-Bitwise-Operators-in-Visual-Basic.md) combine `Boolean` or numeric values and return a result of the same data type as the values.  
  
 The value elements that are combined with an operator are called *operands* of that operator. Operators combined with value elements form expressions, except for the assignment operator, which forms a *statement*. For more information, see [Statements in Visual Basic](../vs140/Statements-in-Visual-Basic.md).  
  
## Evaluation of Expressions  
 The end result of an expression represents a value, which is typically of a familiar data type such as `Boolean`, `String`, or a numeric type.  
  
 The following are examples of expressions.  
  
 `5 + 4`  
  
 `' The preceding expression evaluates to 9.`  
  
 `15 * System.Math.Sqrt(9) + x`  
  
 `' The preceding expression evaluates to 45 plus the value of x.`  
  
 `"Concat" & "ena" & "tion"`  
  
 `' The preceding expression evaluates to "Concatenation".`  
  
 `763 < 23`  
  
 `' The preceding expression evaluates to False.`  
  
 Several operators can perform actions in a single expression or statement, as the following example illustrates.  
  
 [!CODE [VbVbalrOperators#56](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrOperators#56)]  
  
 In the preceding example, [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)] performs the operations in the expression on the right side of the assignment operator (`=`), then assigns the resulting value to the variable `x` on the left. There is no practical limit to the number of operators that can be combined into an expression, but an understanding of [Operator Precedence in Visual Basic](../vs140/Operator-Precedence-in-Visual-Basic.md) is necessary to ensure that you get the results you expect.  
  
 For more information and examples, see [Operator Overloading in Visual Basic 2005](http://go.microsoft.com/fwlink/?LinkId=101703).  
  
## See Also  
 [Operators](../vs140/Operators--Visual-Basic-.md)   
 [Efficient Combination of Operators](../vs140/Efficient-Combination-of-Operators--Visual-Basic-.md)   
 [Statements (Visual Basic)](../vs140/Statements--Visual-Basic-.md)