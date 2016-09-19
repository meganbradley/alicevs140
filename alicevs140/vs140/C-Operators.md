---
title: "C Operators"
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
ms.assetid: 13bc4c8e-2dc9-4b23-9f3a-25064e8777ed
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# C Operators
The C operators are a subset of the [C++ operators](../vs140/C---Operators.md).  
  
 There are three types of operators. A unary expression consists of either a unary operator prepended to an operand, or the `sizeof` keyword followed by an expression. The expression can be either the name of a variable or a cast expression. If the expression is a cast expression, it must be enclosed in parentheses. A binary expression consists of two operands joined by a binary operator. A ternary expression consists of three operands joined by the conditional-expression operator.  
  
 C includes the following unary operators:  
  
|Symbol|Name|  
|------------|----------|  
|**– ~ !**|Negation and complement operators|  
|**\* &**|Indirection and address-of operators|  
|`sizeof`|Size operator|  
|**+**|Unary plus operator|  
|**++ ––**|Unary increment and decrement operators|  
  
 Binary operators associate from left to right. C provides the following binary operators:  
  
|Symbol|Name|  
|------------|----------|  
|**\* / %**|Multiplicative operators|  
|**+ –**|Additive operators|  
|**<< >>**|Shift operators|  
|**<   >   <=   >=   ==   !=**|Relational operators|  
|**&   &#124; ^**|Bitwise operators|  
|**&&   &#124;&#124;**|Logical operators|  
|**,**|Sequential-evaluation operator|  
  
 The base operator (**:>**), supported by previous versions of the Microsoft 16-bit C compiler, is described in [C Language Syntax Summary](../vs140/C-Language-Syntax-Summary.md).  
  
 The conditional-expression operator has lower precedence than binary expressions and differs from them in being right associative.  
  
 Expressions with operators also include assignment expressions, which use unary or binary assignment operators. The unary assignment operators are the increment (`++`) and decrement (**––**) operators; the binary assignment operators are the simple-assignment operator (**=**) and the compound-assignment operators. Each compound-assignment operator is a combination of another binary operator with the simple-assignment operator.  
  
## See Also  
 [Expressions and Assignments](../vs140/Expressions-and-Assignments.md)