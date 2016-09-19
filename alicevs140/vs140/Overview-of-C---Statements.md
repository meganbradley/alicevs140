---
title: "Overview of C++ Statements"
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
ms.assetid: e56996b2-b846-4b99-ac94-ac72fffc5ec7
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Overview of C++ Statements
C++ statements are executed sequentially, except when an expression statement, a selection statement, an iteration statement, or a jump statement specifically modifies that sequence.  
  
 Statements may be of the following types:  
  
```  
  
labeled-statement  
expression-statement  
compound-statement  
selection-statement  
iteration-statement  
jump-statement  
declaration-statement  
try-throw-catch  
  
```  
  
 In most cases, the C++ statement syntax is identical to that of ANSI C. The primary difference between the two is that in C, declarations are allowed only at the start of a block; C++ adds the *declaration-statement*, which effectively removes this restriction. This enables you to introduce variables at a point in the program where a precomputed initialization value can be calculated.  
  
 Declaring variables inside blocks also allows you to exercise precise control over the scope and lifetime of those variables.  
  
 The topics on statements describe the following C++ keywords:  
  
|||||  
|-|-|-|-|  
|[break](../vs140/break-Statement--C---.md)|[else](../vs140/if-else-Statement--C---.md)|[__if_exists](../vs140/__if_exists-Statement.md)|[__try](../vs140/Structured-Exception-Handling--C-C---.md)|  
|[case](../vs140/switch-Statement--C---.md)|[__except](../vs140/Structured-Exception-Handling--C-C---.md)|[__if_not_exists](../vs140/__if_not_exists-Statement.md)|[try](../vs140/try--throw--and-catch-Statements--C---.md)|  
|[catch](../vs140/try--throw--and-catch-Statements--C---.md)|[for](../vs140/for-Statement--C---.md)|[__leave](../vs140/try-finally-Statement--C-.md)|[while](../vs140/while-Statement--C---.md)|  
|[continue](../vs140/continue-Statement--C---.md)|[goto](../vs140/goto-Statement--C---.md)|[return](../vs140/return-Statement--C---.md)||  
|[default](../vs140/switch-Statement--C---.md)|[__finally](../vs140/Structured-Exception-Handling--C-C---.md)|[switch](../vs140/switch-Statement--C---.md)||  
|[do](../vs140/do-while-Statement--C---.md)|[if](../vs140/if-else-Statement--C---.md)|[throw](../vs140/try--throw--and-catch-Statements--C---.md)||  
  
## See Also  
 [Statements](../vs140/Statements--C---.md)