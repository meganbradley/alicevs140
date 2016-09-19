---
title: "Function Body"
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
ms.assetid: f7e74822-fac8-4dc8-8f3a-2b1611da4640
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Function Body
A "function body" is a compound statement containing the statements that specify what the function does.  
  
## Syntax  
 *function-definition*:  
 *declaration-specifiers* opt*attribute-seq* opt*declarator declaration-list* opt*compound-statement*  
  
 /\* *attribute-seq* is Microsoft Specific */  
  
 *compound-statement*: /\* The function body \*/  
 **{**  *declaration-list* opt*statement-list* opt**}**  
  
 Variables declared in a function body, "local variables," have **auto** storage class unless otherwise specified. When the function is called, storage is created for the local variables and local initializations are performed. Execution control passes to the first statement in *compound-statement* and continues until a `return` statement is executed or the end of the function body is encountered. Control then returns to the point at which the function was called.  
  
 A `return` statement containing an expression must be executed if the function is to return a value. The return value of a function is undefined if no `return` statement is executed or if the `return` statement does not include an expression.  
  
## See Also  
 [C Function Definitions](../vs140/C-Function-Definitions.md)