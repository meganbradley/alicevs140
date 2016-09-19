---
title: "Compiler Error C2447"
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
ms.assetid: d1bd6e9a-ee42-4510-ae5e-6b0378f7b931
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C2447
'{' : missing function header (old-style formal list?)  
  
 The compiler encountered an unexpected open brace at global scope. In most cases, this is caused by a badly-formed function header, a misplaced declaration, or a stray semi-colon. To resolve this issue, verify that the open brace follows a correctly-formed function header, and is not preceded by a declaration or a stray semi-colon.  
  
 This error can also be caused by an old-style C-language formal argument list. To resolve this issue, refactor the argument list to use modern style—that is, enclosed in parentheses.  
  
 The following sample generates C2447:  
  
```  
// C2447.cpp  
int c;  
{}       // C2447  
```