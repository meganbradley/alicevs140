---
title: "Postfix Operators"
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
ms.assetid: 76260011-1624-484e-8bef-72ae7ab556cc
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Postfix Operators
The postfix operators have the highest precedence (the tightest binding) in expression evaluation.  
  
## Syntax  
 *postfix-expression*:  
 *primary-expression*  
  
 *postfix-expression*  **[**  *expression*  **]**  
  
 *postfix-expression*  **(**  *argument-expression-list* opt**)**  
  
 *postfix-expression*  **.**  *identifier*  
  
 *postfix-expression*  **–>**  *identifier*  
  
 *postfix-expression*  **++**  
  
 *postfix-expression*  **––**  
  
 Operators in this precedence level are the array subscripts, function calls, structure and union members, and postfix increment and decrement operators.  
  
## See Also  
 [C Operators](../vs140/C-Operators.md)