---
title: "C Additive Operators"
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
ms.assetid: bb8ac205-b061-41fc-8dd4-dab87c8b900c
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# C Additive Operators
The additive operators perform addition (**+**) and subtraction (**–**).  
  
## Syntax  
 *additive-expression*:  
 *multiplicative-expression*  
  
 *additive-expression*  **+**  *multiplicative-expression*  
  
 *additive-expression*  **–**  *multiplicative-expression*  
  
> [!NOTE]
>  Although the syntax for *additive-expression* includes *multiplicative-expression*, this does not imply that expressions using multiplication are required. See the syntax in [C Language Syntax Summary](../vs140/C-Language-Syntax-Summary.md), for *multiplicative-expression*, *cast-expression*, and *unary-expression*.  
  
 The operands can be integral or floating values. Some additive operations can also be performed on pointer values, as outlined under the discussion of each operator.  
  
 The additive operators perform the usual arithmetic conversions on integral and floating operands. The type of the result is the type of the operands after conversion. Since the conversions performed by the additive operators do not provide for overflow or underflow conditions, information may be lost if the result of an additive operation cannot be represented in the type of the operands after conversion.  
  
## See Also  
 [Additive Operators: + and -](../vs140/Additive-Operators----and--.md)