---
title: "Expressions with Unary Operators"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: language-reference
ms.assetid: 1217685b-b85d-4b48-9ff4-d90f56a26c1b
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Expressions with Unary Operators
Unary operators act on only one operand in an expression. The unary operators are as follows:  
  
-   [Indirection operator (*)](../vs140/Indirection-Operator---.md)  
  
-   [Address-of operator (&)](../vs140/Address-of-Operator---.md)  
  
-   [Unary plus operator (+)](../vs140/Unary-Plus-and-Negation-Operators----and--.md)  
  
-   [Unary negation operator (–)](../vs140/Unary-Negation-Operator---.md)  
  
-   [Logical negation operator (!)](../vs140/Logical-Negation-Operator--!.md)  
  
-   [One's complement operator (~)](../vs140/One-s-Complement-Operator--~.md)  
  
-   [Prefix increment operator (++)](../vs140/Prefix-Increment-and-Decrement-Operators-----and---.md)  
  
-   [Prefix decrement operator (––)](../vs140/Prefix-Increment-and-Decrement-Operators-----and---.md)  
  
-   [Cast operator ()](../vs140/Cast-Operator----.md)  
  
-   [sizeof operator](../vs140/sizeof-Operator.md)  
  
-   [__uuidof operator](../vs140/__uuidof-Operator.md)  
  
-   [__alignof operator](../vs140/__alignof-Operator.md)  
  
-   [new operator](../vs140/new-Operator--C---.md)  
  
-   [delete operator](../vs140/delete-Operator--C---.md)  
  
 These operators have right-to-left associativity. Unary expressions generally involve syntax that precedes a postfix or primary expression.  
  
 The following are the possible forms of unary expressions.  
  
-   *postfix-expression*  
  
-   `++` *unary-expression*  
  
-   `––` *unary-expression*  
  
-   *unary-operator* *cast-expression*  
  
-   `sizeof` *unary-expression*  
  
-   `sizeof(` *type-name* `)`  
  
-   `decltype(` *expression* `)`  
  
-   *allocation-expression*  
  
-   *deallocation-expression*  
  
 Any *postfix-expression* is considered a *unary-expression*, and because any primary expression is considered a *postfix-expression*, any primary expressions is considered a *unary-expression* also. For more information, see [Postfix Expressions](../vs140/Postfix-Expressions.md) and [Primary Expressions](../vs140/Primary-Expressions.md).  
  
 A *unary-operator* consists of one or more of the following symbols: `* &``+``–``!``~`  
  
 The *cast-expression* is a unary expression with an optional cast to change the type. For more information see [Cast Operator: ()](../vs140/Cast-Operator----.md).  
  
 An *expression* can be any expression. For more information, see [Expressions (C++)](../vs140/Expressions--C---.md).  
  
 The *allocation-expression* refers to the `new` operator. The *deallocation-expression* refers to the `delete` operator. For more information, see the links earlier in this topic.  
  
## See Also  
 [Types of Expressions](../vs140/Types-of-Expressions.md)