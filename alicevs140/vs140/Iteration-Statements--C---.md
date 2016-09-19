---
title: "Iteration Statements (C++)"
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
ms.assetid: bf6d75f7-ead2-426a-9c47-33847f59b8c7
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Iteration Statements (C++)
Iteration statements cause statements (or compound statements) to be executed zero or more times, subject to some loop-termination criteria. When these statements are compound statements, they are executed in order, except when either the [break](../vs140/break-Statement--C---.md) statement or the [continue](../vs140/continue-Statement--C---.md) statement is encountered.  
  
 C++ provides four iteration statements — [while](../vs140/while-Statement--C---.md), [do](../vs140/do-while-Statement--C---.md), [for](../vs140/for-Statement--C---.md), and [range-based for](../vs140/Range-based-for-Statement--C---.md). Each of these iterates until its termination expression evaluates to zero (false), or until loop termination is forced with a **break** statement. The following table summarizes these statements and their actions; each is discussed in detail in the sections that follow.  
  
### Iteration Statements  
  
|Statement|Evaluated At|Initialization|Increment|  
|---------------|------------------|--------------------|---------------|  
|`while`|Top of loop|No|No|  
|**do**|Bottom of loop|No|No|  
|**for**|Top of loop|Yes|Yes|  
|**range-based for**|Top of loop|Yes|Yes|  
  
 The statement part of an iteration statement cannot be a declaration. However, it can be a compound statement containing a declaration.  
  
## See Also  
 [Overview of C++ Statements](../vs140/Overview-of-C---Statements.md)