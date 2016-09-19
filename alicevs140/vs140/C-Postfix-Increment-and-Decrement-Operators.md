---
title: "C Postfix Increment and Decrement Operators"
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
ms.assetid: 56ba218d-65f9-405f-8684-caccc0ca33aa
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# C Postfix Increment and Decrement Operators
Operands of the postfix increment and decrement operators are scalar types that are modifiable l-values.  
  
## Syntax  
 *postfix-expression*:  
 *postfix-expression*  **++**  
  
 *postfix-expression*  **––**  
  
 The result of the postfix increment or decrement operation is the value of the operand. After the result is obtained, the value of the operand is incremented (or decremented). The following code illustrates the postfix increment operator.  
  
```  
if( var++ > 0 )  
    *p++ = *q++;  
```  
  
 In this example, the variable `var` is compared to 0, then incremented. If `var` was positive before being incremented, the next statement is executed. First, the value of the object pointed to by `q` is assigned to the object pointed to by `p`. Then, `q` and `p` are incremented.  
  
## See Also  
 [Postfix Increment and Decrement Operators: ++ and --](../vs140/Postfix-Increment-and-Decrement-Operators-----and---.md)