---
title: "Prefix Increment and Decrement Operators"
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
ms.assetid: 9a441bb9-d94a-4b6a-9db2-0d0d76bc480d
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Prefix Increment and Decrement Operators
The unary operators (`++` and **––**) are called "prefix" increment or decrement operators when the increment or decrement operators appear before the operand. Postfix increment and decrement has higher precedence than prefix increment and decrement. The operand must have integral, floating, or pointer type and must be a modifiable l-value expression (an expression without the **const** attribute). The result is an l-value.  
  
 When the operator appears before its operand, the operand is incremented or decremented and its new value is the result of the expression.  
  
 An operand of integral or floating type is incremented or decremented by the integer value 1. The type of the result is the same as the operand type. An operand of pointer type is incremented or decremented by the size of the object it addresses. An incremented pointer points to the next object; a decremented pointer points to the previous object.  
  
## Example  
 This example illustrates the unary prefix decrement operator:  
  
```  
if( line[--i] != '\n' )  
    return;  
```  
  
 In this example, the variable `i` is decremented before it is used as a subscript to `line`.  
  
## See Also  
 [C Unary Operators](../vs140/C-Unary-Operators.md)