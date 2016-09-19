---
title: "Overloading Unary Operators"
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
ms.assetid: 7683ef08-42a4-4283-928f-d3dd4f3ab4c0
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Overloading Unary Operators
The unary operators that can be overloaded are the following:  
  
1.  `!` ([logical NOT](../vs140/Logical-Negation-Operator--!.md))  
  
2.  `&` ([address-of](../vs140/Address-of-Operator---.md))  
  
3.  `~` ([one's complement](../vs140/One-s-Complement-Operator--~.md))  
  
4.  `*` ([pointer dereference](../vs140/Indirection-Operator---.md))  
  
5.  `+` ([unary plus](../vs140/Additive-Operators----and--.md))  
  
6.  `-` ([unary negation](../vs140/Additive-Operators----and--.md))  
  
7.  `++` ([increment](../vs140/Prefix-Increment-and-Decrement-Operators-----and---.md))  
  
8.  `--` ([decrement](../vs140/Prefix-Increment-and-Decrement-Operators-----and---.md))  
  
9. conversion operators  
  
 The postfix increment and decrement operators (`++` and **––**) are treated separately in [Increment and Decrement](../vs140/Increment-and-Decrement-Operator-Overloading--C---.md).  
  
 Conversion operators are also discussed in a separate topic; see [Conversions](../vs140/User-Defined-Type-Conversions--C---.md).  
  
 The following rules are true of all other unary operators. To declare a unary operator function as a nonstatic member, you must declare it in the form:  
  
 `ret-type operator` `op` `()`  
  
 where `ret-type` is the return type and `op` is one of the operators listed in the preceding table.  
  
 To declare a unary operator function as a global function, you must declare it in the form:  
  
 `ret-type operator` `op` (`arg` )  
  
 where `ret-type` and `op` are as described for member operator functions and the `arg` is an argument of class type on which to operate.  
  
> [!NOTE]
>  There is no restriction on the return types of the unary operators. For example, it makes sense for logical NOT (`!`) to return an integral value, but this is not enforced.  
  
## See Also  
 [Operator Overloading](../vs140/Operator-Overloading.md)