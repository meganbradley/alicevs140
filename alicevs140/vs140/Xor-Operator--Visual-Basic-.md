---
title: "Xor Operator (Visual Basic)"
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
ms.assetid: 036000a9-3934-4e7f-a9d0-a816de3d84a6
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Xor Operator (Visual Basic)
Performs a logical exclusion on two `Boolean` expressions, or a bitwise exclusion on two numeric expressions.  
  
## Syntax  
  
```  
  
result = expression1 Xor expression2  
```  
  
## Parts  
 `result`  
 Required. Any `Boolean` or numeric variable. For Boolean comparison, `result` is the logical exclusion (exclusive logical disjunction) of two `Boolean` values. For bitwise operations, `result` is a numeric value that represents the bitwise exclusion (exclusive bitwise disjunction) of two numeric bit patterns.  
  
 `expression1`  
 Required. Any `Boolean` or numeric expression.  
  
 `expression2`  
 Required. Any `Boolean` or numeric expression.  
  
## Remarks  
 For Boolean comparison, `result` is `True` if and only if exactly one of `expression1` and `expression2` evaluates to `True`. That is, if and only if `expression1` and `expression2` evaluate to opposite `Boolean` values. The following table illustrates how `result` is determined.  
  
|If `expression1` is|And `expression2` is|The value of `result` is|  
|-------------------------|--------------------------|------------------------------|  
|`True`|`True`|`False`|  
|`True`|`False`|`True`|  
|`False`|`True`|`True`|  
|`False`|`False`|`False`|  
  
> [!NOTE]
>  In a Boolean comparison, the `Xor` operator always evaluates both expressions, which could include making procedure calls. There is no short-circuiting counterpart to `Xor`, because the result always depends on both operands. For *short-circuiting* logical operators, see [AndAlso Operator](../vs140/AndAlso-Operator--Visual-Basic-.md) and [OrElse Operator](../vs140/OrElse-Operator--Visual-Basic-.md).  
  
 For bitwise operations, the `Xor` operator performs a bitwise comparison of identically positioned bits in two numeric expressions and sets the corresponding bit in `result` according to the following table.  
  
|If bit in `expression1` is|And bit in `expression2` is|The bit in `result` is|  
|--------------------------------|---------------------------------|----------------------------|  
|1|1|0|  
|1|0|1|  
|0|1|1|  
|0|0|0|  
  
> [!NOTE]
>  Since the logical and bitwise operators have a lower precedence than other arithmetic and relational operators, any bitwise operations should be enclosed in parentheses to ensure accurate execution.  
  
 For example, 5 `Xor` 3 is 6. To see why this is so, convert 5 and 3 to their binary representations, 101 and 011. Then use the previous table to determine that 101 Xor 011 is 110, which is the binary representation of the decimal number 6.  
  
## Data Types  
 If the operands consist of one `Boolean` expression and one numeric expression, Visual Basic converts the `Boolean` expression to a numeric value (–1 for `True` and 0 for `False`) and performs a bitwise operation.  
  
 For a `Boolean` comparison, the data type of the result is `Boolean`. For a bitwise comparison, the result data type is a numeric type appropriate for the data types of `expression1` and `expression2`. See the "Relational and Bitwise Comparisons" table in [Data Types of Operator Results](../Topic/Data%20Types%20of%20Operator%20Results%20\(Visual%20Basic\).md).  
  
## Overloading  
 The `Xor` operator can be *overloaded*, which means that a class or structure can redefine its behavior when an operand has the type of that class or structure. If your code uses this operator on such a class or structure, make sure you understand its redefined behavior. For more information, see [Operator Procedures](../vs140/Operator-Procedures--Visual-Basic-.md).  
  
## Example  
 The following example uses the `Xor` operator to perform logical exclusion (exclusive logical disjunction) on two expressions. The result is a `Boolean` value that represents whether exactly one of the expressions is `True`.  
  
 [!CODE [VbVbalrOperators#40](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrOperators#40)]  
  
 The previous example produces results of `False`, `True`, and `False`, respectively.  
  
## Example  
 The following example uses the `Xor` operator to perform logical exclusion (exclusive logical disjunction) on the individual bits of two numeric expressions. The bit in the result pattern is set if exactly one of the corresponding bits in the operands is set to 1.  
  
 [!CODE [VbVbalrOperators#41](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrOperators#41)]  
  
 The previous example produces results of 2, 12, and 14, respectively.  
  
## See Also  
 [Logical/Bitwise Operators (Visual Basic)](../vs140/Logical-Bitwise-Operators--Visual-Basic-.md)   
 [Operator Precedence in Visual Basic](../vs140/Operator-Precedence-in-Visual-Basic.md)   
 [Operators Listed by Functionality](../vs140/Operators-Listed-by-Functionality--Visual-Basic-.md)   
 [Logical and Bitwise Operators in Visual Basic](../vs140/Logical-and-Bitwise-Operators-in-Visual-Basic.md)