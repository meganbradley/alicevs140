---
title: "Type Conversions (C)"
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
ms.assetid: d130ee7c-03c3-48f4-af7b-1fdba0d3b086
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Type Conversions (C)
Type conversions depend on the specified operator and the type of the operand or operators. Type conversions are performed in the following cases:  
  
-   When a value of one type is assigned to a variable of a different type or an operator converts the type of its operand or operands before performing an operation  
  
-   When a value of one type is explicitly cast to a different type  
  
-   When a value is passed as an argument to a function or when a type is returned from a function  
  
 A character, a short integer, or an integer bit field, all either signed or not, or an object of enumeration type, can be used in an expression wherever an integer can be used. If an `int` can represent all the values of the original type, then the value is converted to `int`; otherwise, it is converted to `unsigned int`. This process is called "integral promotion." Integral promotions preserve value. That is, the value after promotion is guaranteed to be the same as before the promotion. See [Usual Arithmetic Conversions](../vs140/Usual-Arithmetic-Conversions.md) for more information.  
  
## See Also  
 [Expressions and Assignments](../vs140/Expressions-and-Assignments.md)