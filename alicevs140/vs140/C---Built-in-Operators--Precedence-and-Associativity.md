---
title: "C++ Built-in Operators, Precedence and Associativity"
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
ms.assetid: 95c1f0ba-dad8-4034-b039-f79a904f112f
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# C++ Built-in Operators, Precedence and Associativity
The C++ language includes all C operators and adds several new operators. Operators specify an evaluation to be performed on one or more operands.  
  
 Operator precedence specifies the order of operations in expressions that contain more than one operator. Operator associativity specifies whether, in an expression that contains multiple operators with the same precedence, an operand is grouped with the one on its left or the one on its right. The following table shows the precedence and associativity of C++ operators (from highest to lowest precedence). Operators with the same precedence number have equal precedence unless another relationship is explicitly forced by parentheses.  
  
### C++ Operator Precedence and Associativity  
  
|Operator Description|Operator|  
|--------------------------|--------------|  
|`Group 1 precedence, no associativity`|  
|[Scope resolution](../vs140/Scope-Resolution-Operator----.md)|`::`|  
|`Group 2 precedence, left to right associativity`|  
|[Member selection (object or pointer)](../vs140/Member-Access-Operators--.-and---.md)|`. or –>`|  
|[Array subscript](../vs140/Subscript-Operator-.md)|`[ ]`|  
|[Function call](../vs140/Function-Call-Operator----.md)|`( )`|  
|[Postfix increment](../vs140/Postfix-Increment-and-Decrement-Operators-----and---.md)|`++`|  
|[Postfix decrement](../vs140/Postfix-Increment-and-Decrement-Operators-----and---.md)|`––`|  
|[Type name](../Topic/typeid%20Operator.md)|`typeid( )`|  
|[Constant type conversion](../vs140/const_cast-Operator.md)|`const_cast`|  
|[Dynamic type conversion](../vs140/dynamic_cast-Operator.md)|`dynamic_cast`|  
|[Reinterpreted type conversion](../vs140/reinterpret_cast-Operator.md)|`reinterpret_cast`|  
|[Static type conversion](../vs140/static_cast-Operator.md)|`static_cast`|  
|`Group 3 precedence, right to left associativity`|  
|[Size of object or type](../vs140/sizeof-Operator.md)|`sizeof`|  
|[Prefix increment](../vs140/Prefix-Increment-and-Decrement-Operators-----and---.md)|`++`|  
|[Prefix decrement](../vs140/Prefix-Increment-and-Decrement-Operators-----and---.md)|`––`|  
|[One's complement](../vs140/One-s-Complement-Operator--~.md)|`~`|  
|[Logical not](../vs140/Logical-Negation-Operator--!.md)|`!`|  
|[Unary negation](../vs140/Unary-Negation-Operator---.md)|`-`|  
|[Unary plus](../vs140/Unary-Plus-and-Negation-Operators----and--.md)|`+`|  
|[Address-of](../vs140/Lvalue-Reference-Declarator---.md)|`&`|  
|[Indirection](../vs140/Indirection-Operator---.md)|`*`|  
|[Create object](../vs140/new-Operator--C---.md)|`new`|  
|[Destroy object](../vs140/delete-Operator--C---.md)|`delete`|  
|[Cast](../vs140/Cast-Operator----.md)|`Cast: ()`|  
|`Group 4 precedence, left to right associativity`|  
|[Pointer-to-member (objects or pointers)](../vs140/Pointer-to-Member-Operators--.--and----.md)|`.* or –>*`|  
|`Group 5 precedence, left to right associativity`|  
|[Multiplication](../vs140/Multiplicative-Operators-and-the-Modulus-Operator.md)|`*`|  
|[Division](../vs140/Multiplicative-Operators-and-the-Modulus-Operator.md)|`/`|  
|[Modulus](../vs140/Multiplicative-Operators-and-the-Modulus-Operator.md)|`%`|  
|`Group 6 precedence, left to right associativity`|  
|[Addition](../vs140/Additive-Operators----and--.md)|`+`|  
|[Subtraction](../vs140/Additive-Operators----and--.md)|`–`|  
|`Group 7 precedence, left to right associativity`|  
|[Left shift](../vs140/Left-Shift-and-Right-Shift-Operators-----and----.md)|`<<`|  
|[Right shift](../vs140/Left-Shift-and-Right-Shift-Operators-----and----.md)|`>>`|  
|`Group 8 precedence, left to right associativity`|  
|[Less than](../vs140/Relational-Operators---------=--and--=.md)|`<`|  
|[Greater than](../vs140/Relational-Operators---------=--and--=.md)|`>`|  
|[Less than or equal to](../vs140/Relational-Operators---------=--and--=.md)|`<=`|  
|[Greater than or equal to](../vs140/Relational-Operators---------=--and--=.md)|`>=`|  
|`Group 9 precedence, left to right associativity`|  
|[Equality](../vs140/Equality-Operators--==-and-!=.md)|`==`|  
|[Inequality](../vs140/Equality-Operators--==-and-!=.md)|`!=`|  
|`Group 10 precedence left to right associativity`|  
|[Bitwise AND](../vs140/Bitwise-AND-Operator---.md)|`&`|  
|`Group 11 precedence, left to right associativity`|  
|[Bitwise exclusive OR](../vs140/Bitwise-Exclusive-OR-Operator--^.md)|`^`|  
|`Group 12 precedence, left to right associativity`|  
|[Bitwise inclusive OR](../vs140/Bitwise-Inclusive-OR-Operator---.md)|`&#124;`|  
|`Group 13 precedence, left to right associativity`|  
|[Logical AND](../vs140/Logical-AND-Operator----.md)|`&&`|  
|`Group 14 precedence, left to right associativity`|  
|[Logical OR](../vs140/Logical-OR-Operator----.md)|`&#124;&#124;`|  
|`Group 15 precedence, right to left associativity`|  
|[Conditional](../vs140/Conditional-Operator-----.md)|`? :`|  
|`Group 16 precedence, right to left associativity`|  
|[Assignment](../vs140/Assignment-Operators.md)|`=`|  
|[Multiplication assignment](../vs140/Assignment-Operators.md)|`*=`|  
|[Division assignment](../vs140/Assignment-Operators.md)|`/=`|  
|[Modulus assignment](../vs140/Assignment-Operators.md)|`%=`|  
|[Addition assignment](../vs140/Assignment-Operators.md)|`+=`|  
|[Subtraction assignment](../vs140/Assignment-Operators.md)|`–=`|  
|[Left-shift assignment](../vs140/Assignment-Operators.md)|`<<=`|  
|[Right-shift assignment](../vs140/Assignment-Operators.md)|`>>=`|  
|[Bitwise AND assignment](../vs140/Assignment-Operators.md)|`&=`|  
|[Bitwise inclusive OR assignment](../vs140/Assignment-Operators.md)|`&#124;=`|  
|[Bitwise exclusive OR assignment](../vs140/Assignment-Operators.md)|`^=`|  
|`Group 17 precedence, right to left associativity`|  
|[throw expression](../vs140/try--throw--and-catch-Statements--C---.md)|`throw`|  
|`Group 18 precedence, left to right associativity`|  
|[Comma](../vs140/Comma-Operator---.md)|`,`|  
  
## See Also  
 [C++ Operators](../vs140/C---Operators.md)   
 [Operator Overloading](../vs140/Operator-Overloading.md)