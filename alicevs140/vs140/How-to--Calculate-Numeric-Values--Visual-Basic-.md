---
title: "How to: Calculate Numeric Values (Visual Basic)"
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
ms.assetid: ba6bf43d-bd96-49b8-b1de-4a7797551372
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Calculate Numeric Values (Visual Basic)
You can calculate numeric values through the use of numeric expressions. A *numeric expression* is an expression that contains literals, constants, and variables representing numeric values, and operators that act on those values.  
  
## Calculating Numeric Values  
  
#### To calculate a numeric value  
  
-   Combine one or more numeric literals, constants, and variables into a numeric expression. The following example shows some valid numeric expressions.  
  
     `93.217`  
  
     `System.Math.PI`  
  
     `counter`  
  
     `4 * (67 + i)`  
  
     The first three lines show a literal, a constant, and a variable. Each one forms a valid numeric expression by itself. The final line shows a combination of a variable with two literals.  
  
     Note that a numeric expression does not form a complete [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)] statement by itself. You must use the expression as part of a complete statement.  
  
#### To store a numeric value  
  
-   You can use an assignment statement to assign the value represented by a numeric expression to a variable, as the following example demonstrates.  
  
     [!CODE [VbVbalrOperators#82](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrOperators#82)]  
  
     In the preceding example, the value of the expression on the right side of the equal operator (`=`) is assigned to the variable `j` on the left side of the operator, so `j` evaluates to 276.  
  
     For more information, see [Statements (Visual Basic)](../vs140/Statements--Visual-Basic-.md).  
  
## Multiple Operators  
 If the numeric expression contains more than one operator, the order in which they are evaluated is determined by the rules of operator precedence. To override the rules of operator precedence, you enclose expressions in parentheses, as in the above example; the enclosed expressions are evaluated first.  
  
#### To override normal operator precedence  
  
-   Use parentheses to enclose the operations you want to be performed first. The following example shows two different results with the same operands and operators.  
  
     [!CODE [VbVbalrOperators#83](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrOperators#83)]  
  
     In the preceding example, the calculation for `j` performs the addition operator (`+`) first because the parentheses around `(67 + i)` override normal precedence, and the value assigned to `j` is 276 (4 times 69). The calculation for `k` performs the operators in their normal precedence (`*` before `+`), and the value assigned to `k` is 270 (268 plus 2).  
  
     For more information, see [Operator Precedence in Visual Basic](../vs140/Operator-Precedence-in-Visual-Basic.md).  
  
## See Also  
 [Operators and Expressions in Visual Basic](../vs140/Operators-and-Expressions-in-Visual-Basic.md)   
 [Value Comparisons](../vs140/Value-Comparisons--Visual-Basic-.md)   
 [Statements (Visual Basic)](../vs140/Statements--Visual-Basic-.md)   
 [Operator Precedence in Visual Basic](../vs140/Operator-Precedence-in-Visual-Basic.md)   
 [Arithmetic Operators](../vs140/Arithmetic-Operators--Visual-Basic-.md)   
 [Efficient Combination of Operators](../vs140/Efficient-Combination-of-Operators--Visual-Basic-.md)