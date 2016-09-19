---
title: "Fatal Error C1061"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: error-reference
ms.assetid: 9366c0bc-96e0-4967-aa7d-4ebf098de806
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Fatal Error C1061
compiler limit : blocks nested too deeply  
  
 Nesting of code blocks exceeds the limit of 128 nesting levels. This is a hard limit in the compiler for both C and C++, in both the 32-bit and 64-bit tool set. The count of nesting levels can be increased by anything that creates a scope or block. For example, namespaces, using directives, preprocessor expansions, template expansion, exception handling, loop constructs, and else-if clauses can all increase the nesting level seen by the compiler.  
  
 To fix this error you must refactor your code. In any case, deeply nested code is difficult to understand and reason about. Refactoring your code to have fewer nesting levels may improve code quality and simplify maintenance. Break deeply nested code into functions that are called from the original context. Limit the number of loops or chained else-if clauses within a block.