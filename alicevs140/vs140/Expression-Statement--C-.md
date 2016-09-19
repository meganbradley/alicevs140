---
title: "Expression Statement (C)"
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
ms.assetid: 1085982b-dc16-4c1e-9ddd-0cd85c8fe2e3
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Expression Statement (C)
When an expression statement is executed, the expression is evaluated according to the rules outlined in [Expressions and Assignments](../vs140/Expressions-and-Assignments.md).  
  
## Syntax  
 *expression-statement*:  
 *expression* opt**;**  
  
 All side effects from the expression evaluation are completed before the next statement is executed. An empty expression statement is called a null statement. See [The Null Statement](../vs140/Null-Statement--C-.md) for more information.  
  
 These examples demonstrate expression statements.  
  
```  
x = ( y + 3 );            /* x is assigned the value of y + 3  */  
x++;                      /* x is incremented                  */  
x = y = 0;                /* Both x and y are initialized to 0 */  
proc( arg1, arg2 );       /* Function call returning void      */  
y = z = ( f( x ) + 3 );   /* A function-call expression        */  
```  
  
 In the last statement, the function-call expression, the value of the expression, which includes any value returned by the function, is increased by 3 and then assigned to both the variables `y` and `z`.  
  
## See Also  
 [Statements (C)](../vs140/Statements--C-.md)