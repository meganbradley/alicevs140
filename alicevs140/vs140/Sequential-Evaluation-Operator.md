---
title: "Sequential-Evaluation Operator"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
  - C
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 587514f4-c8e2-44e9-81a8-7a553ce1453a
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Sequential-Evaluation Operator
The sequential-evaluation operator, also called the "comma operator," evaluates its two operands sequentially from left to right.  
  
## Syntax  
 *expression*:  
 *assignment-expression*  
  
 *expression*  **,**  *assignment-expression*  
  
 The left operand of the sequential-evaluation operator is evaluated as a `void` expression. The result of the operation has the same value and type as the right operand. Each operand can be of any type. The sequential-evaluation operator does not perform type conversions between its operands, and it does not yield an l-value. There is a sequence point after the first operand, which means all side effects from the evaluation of the left operand are completed before beginning evaluation of the right operand. See [Sequence Points](../vs140/C-Sequence-Points.md) for more information.  
  
 The sequential-evaluation operator is typically used to evaluate two or more expressions in contexts where only one expression is allowed.  
  
 Commas can be used as separators in some contexts. However, you must be careful not to confuse the use of the comma as a separator with its use as an operator; the two uses are completely different.  
  
## Example  
 This example illustrates the sequential-evaluation operator:  
  
```  
for ( i = j = 1; i + j < 20; i += i, j-- );  
```  
  
 In this example, each operand of the **for** statement's third expression is evaluated independently. The left operand `i += i` is evaluated first; then the right operand, `j––`, is evaluated.  
  
```  
func_one( x, y + 2, z );  
func_two( (x--, y + 2), z );  
```  
  
 In the function call to `func_one`, three arguments, separated by commas, are passed: `x`, `y + 2`, and `z`. In the function call to `func_two`, parentheses force the compiler to interpret the first comma as the sequential-evaluation operator. This function call passes two arguments to `func_two`. The first argument is the result of the sequential-evaluation operation `(x--, y + 2)`, which has the value and type of the expression `y + 2`; the second argument is `z`.  
  
## See Also  
 [Comma Operator: ,](../vs140/Comma-Operator---.md)