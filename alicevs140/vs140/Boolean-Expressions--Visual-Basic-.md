---
title: "Boolean Expressions (Visual Basic)"
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
ms.assetid: d3d90406-55c8-4404-8143-50fd7f0d0d1a
caps.latest.revision: 21
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Boolean Expressions (Visual Basic)
A *Boolean expression* is an expression that evaluates to a value of the [Boolean Data Type](../vs140/Boolean-Data-Type--Visual-Basic-.md): `True` or `False`. `Boolean` expressions can take several forms. The simplest is the direct comparison of the value of a `Boolean` variable to a `Boolean` literal, as shown in the following example.  
  
 [!CODE [VbVbalrOperators#87](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrOperators#87)]  
  
## Two Meanings of the = Operator  
 Notice that the assignment statement `newCustomer = True` looks the same as the expression in the preceding example, but it performs a different function and is used differently. In the preceding example, the expression `newCustomer = True` represents a Boolean value, and the `=` sign is interpreted as a comparison operator. In a stand-alone statement, the `=` sign is interpreted as an assignment operator and assigns the value on the right to the variable on the left. The following example illustrates this.  
  
 [!CODE [VbVbalrOperators#88](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrOperators#88)]  
  
 For further information, see [Value Comparisons](../vs140/Value-Comparisons--Visual-Basic-.md) and [Statements (Visual Basic)](../vs140/Statements--Visual-Basic-.md).  
  
## Comparison Operators  
 Comparison operators such as `=`, `<`, `>`, `<>`, `<=`, and `>=` produce Boolean expressions by comparing the expression on the left side of the operator to the expression on the right side of the operator and evaluating the result as `True` or `False`. The following example illustrates this.  
  
 `42 < 81`  
  
 Because 42 is less than 81, the Boolean expression in the preceding example evaluates to `True`. For more information on this kind of expression, see [Value Comparisons](../vs140/Value-Comparisons--Visual-Basic-.md).  
  
### Comparison Operators Combined with Logical Operators  
 Comparison expressions can be combined using logical operators to produce more complex Boolean expressions. The following example demonstrates the use of comparison operators in conjunction with a logical operator.  
  
 `x > y And x < 1000`  
  
 In the preceding example, the value of the overall expression depends on the values of the expressions on each side of the `And` operator. If both expressions are `True`, then the overall expression evaluates to `True`. If either expression is `False`, then the entire expression evaluates to `False`.  
  
## Short-Circuiting Operators  
 The logical operators `AndAlso` and `OrElse` exhibit behavior known as *short-circuiting*. A short-circuiting operator evaluates the left operand first. If the left operand determines the value of the entire expression, then program execution proceeds without evaluating the right expression. The following example illustrates this.  
  
 [!CODE [VbVbalrOperators#89](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrOperators#89)]  
  
 In the preceding example, the operator evaluates the left expression, `45 < 12`. Because the left expression evaluates to `False`, the entire logical expression must evaluate to `False`. Program execution thus skips execution of the code within the `If` block without evaluating the right expression, `testFunction(3)`. This example does not call `testFunction()` because the left expression falsifies the entire expression.  
  
 Similarly, if the left expression in a logical expression using `OrElse` evaluates to `True`, execution proceeds to the next line of code without evaluating the right expression, because the left expression has already validated the entire expression.  
  
### Comparison with Non-Short-Circuiting Operators  
 By contrast, both sides of the logical operator are evaluated when the logical operators `And` and `Or` are used. The following example illustrates this.  
  
 [!CODE [VbVbalrOperators#90](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrOperators#90)]  
  
 The preceding example calls `testFunction()` even though the left expression evaluates to `False`.  
  
## Parenthetical Expressions  
 You can use parentheses to control the order of evaluation of Boolean expressions. Expressions enclosed by parentheses evaluate first. For multiple levels of nesting, precedence is granted to the most deeply nested expressions. Within parentheses, evaluation proceeds according to the rules of operator precedence. For more information, see [Operator Precedence in Visual Basic](../vs140/Operator-Precedence-in-Visual-Basic.md).  
  
## See Also  
 [Logical and Bitwise Operators in Visual Basic](../vs140/Logical-and-Bitwise-Operators-in-Visual-Basic.md)   
 [Value Comparisons](../vs140/Value-Comparisons--Visual-Basic-.md)   
 [Statements in Visual Basic](../vs140/Statements-in-Visual-Basic.md)   
 [Comparison Operators](../Topic/Comparison%20Operators%20\(Visual%20Basic\).md)   
 [Efficient Combination of Operators](../vs140/Efficient-Combination-of-Operators--Visual-Basic-.md)   
 [Operator Precedence in Visual Basic](../vs140/Operator-Precedence-in-Visual-Basic.md)   
 [Boolean Data Type (Visual Basic)](../vs140/Boolean-Data-Type--Visual-Basic-.md)