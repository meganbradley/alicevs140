---
title: "Function Call (C)"
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
ms.assetid: 35c66719-3f15-4d3b-97da-4e19dc97b308
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Function Call (C)
A "function call" is an expression that includes the name of the function being called or the value of a function pointer and, optionally, the arguments being passed to the function.  
  
## Syntax  
 *postfix-expression*:  
 *postfix-expression*  **(**  *argument-expression-list* opt**)**  
  
 *argument-expression-list*:  
 *assignment-expression*  
  
 *argument-expression-list*  **,**  *assignment-expression*  
  
 The *postfix-expression* must evaluate to a function address (for example, a function identifier or the value of a function pointer), and *argument-expression-list* is a list of expressions (separated by commas) whose values (the "arguments") are passed to the function. The *argument-expression-list* argument can be empty.  
  
 A function-call expression has the value and type of the function's return value. A function cannot return an object of array type. If the function's return type is `void` (that is, the function has been declared never to return a value), the function-call expression also has `void` type. (See [Function Calls](../vs140/Function-Calls.md) for more information.)  
  
## See Also  
 [Function Call Operator: ()](../vs140/Function-Call-Operator----.md)