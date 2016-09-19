---
title: "Overview of C Statements"
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
ms.assetid: 0d49837a-5399-4881-b60c-af5f4e9720de
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Overview of C Statements
C statements consist of tokens, expressions, and other statements. A statement that forms a component of another statement is called the "body" of the enclosing statement. Each statement type given by the following syntax is discussed in this section.  
  
## Syntax  
 *statement*:  
 [labeled-statement](../vs140/goto-and-Labeled-Statements--C-.md)  
  
 [compound-statement](../vs140/Compound-Statement--C-.md)  
  
 [expression-statement](../vs140/Expression-Statement--C-.md)  
  
 [selection-statement](../vs140/if-Statement--C-.md)  
  
 [iteration-statement](../vs140/do-while-Statement--C-.md)  
  
 [jump-statement](../vs140/break-Statement--C-.md)  
  
 [try-except-statement](../vs140/try-except-Statement--C-.md)  
  
 /* Microsoft Specific \*/[try-finally-statement](../vs140/try-finally-Statement--C-.md) /\* Microsoft Specific \*/  
  
 Frequently the statement body is a "compound statement." A compound statement consists of other statements that can include keywords. The compound statement is delimited by braces (**{ }**). All other C statements end with a semicolon (**;**). The semicolon is a statement terminator.  
  
 The expression statement contains a C expression that can contain the arithmetic or logical operators introduced in [Expressions and Assignments](../vs140/Expressions-and-Assignments.md). The null statement is an empty statement.  
  
 Any C statement can begin with an identifying label consisting of a name and a colon. Since only the `goto` statement recognizes statement labels, statement labels are discussed with `goto`. See [The goto and Labeled Statements](../vs140/goto-and-Labeled-Statements--C-.md) for more information.  
  
## See Also  
 [Statements (C)](../vs140/Statements--C-.md)