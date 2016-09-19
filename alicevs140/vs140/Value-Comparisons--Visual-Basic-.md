---
title: "Value Comparisons (Visual Basic)"
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
ms.assetid: 60da0c76-9458-4afc-97e9-44a7939c064c
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Value Comparisons (Visual Basic)
Comparison operators can be used to construct expressions that compare the values of numeric variables. These expressions return a `Boolean` value based on whether the comparison is true or false. Examples of such an expression are as follows.  
  
 `45 > 26`  
  
 `26 > 45`  
  
 The first expression evaluates to `True`, because 45 is greater than 26. The second example evaluates to `False`, because 26 is not greater than 45.  
  
 You can also compare numeric expressions in this fashion. The expressions you compare can themselves be complex expressions, as in the following example.  
  
 `x / 45 * (y +17) >= System.Math.Sqrt(z) / (p - (x * 16))`  
  
 The preceding complex expression includes literals, variables, and function calls. The expressions on both sides of the comparison operator are evaluated, and the resulting values are then compared using the `>=` comparison operator. If the value of the expression on the left side is greater than or equal to the value of the expression on the right, the entire expression evaluates to `True`; otherwise, it evaluates to `False`.  
  
 Expressions that compare values are most commonly used in `If...Then` constructions, as in the following example.  
  
 [!CODE [VbVbalrOperators#84](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrOperators#84)]  
  
 The `=` sign is a comparison operator as well as an assignment operator. When used as a comparison operator, it evaluates whether the value on the left is equal to the value on the right, as shown in the following example.  
  
 [!CODE [VbVbalrOperators#85](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrOperators#85)]  
  
 You can also use a comparison expression anywhere a `Boolean` value is needed, such as in an `If`, `While`, `Loop`, or `ElseIf` statement, or when assigning to or passing a value to a `Boolean` variable. In the following example, the value returned by the comparison expression is assigned to a `Boolean` variable.  
  
 [!CODE [VbVbalrOperators#86](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrOperators#86)]  
  
## See Also  
 [Boolean Expressions](../vs140/Boolean-Expressions--Visual-Basic-.md)   
 [Operators and Expressions in Visual Basic](../vs140/Operators-and-Expressions-in-Visual-Basic.md)   
 [Comparison Operators in Visual Basic](../vs140/Comparison-Operators-in-Visual-Basic.md)   
 [How to: Calculate Numeric Values](../vs140/How-to--Calculate-Numeric-Values--Visual-Basic-.md)   
 [Operator Precedence in Visual Basic](../vs140/Operator-Precedence-in-Visual-Basic.md)