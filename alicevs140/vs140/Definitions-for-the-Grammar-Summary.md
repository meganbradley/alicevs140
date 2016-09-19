---
title: "Definitions for the Grammar Summary"
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
ms.assetid: cc752dc8-6f4e-4347-a556-e0d9ef4c46bd
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Definitions for the Grammar Summary
Terminals are endpoints in a syntax definition. No other resolution is possible. Terminals include the set of reserved words and user-defined identifiers.  
  
 Nonterminals are placeholders in the syntax. Most are defined elsewhere in this syntax summary. Definitions can be recursive. The following nonterminals are defined in the [Grammar Summary](../vs140/Grammar-Summary--C---.md) of the *C++ Language Reference*:  
  
 `constant`, *constant-expression*, *identifier*, *keyword*, `operator`, `punctuator`  
  
 An optional component is indicated by the subscripted opt. For example, the following indicates an optional expression enclosed in curly braces:  
  
 **{** *expression*opt **}**  
  
## See Also  
 [Grammar Summary (C/C++)](../vs140/Grammar-Summary--C-C---.md)