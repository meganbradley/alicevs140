---
title: "Compiler Error C2735"
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
ms.assetid: 6ce45600-7148-4bc0-8699-af0ef137571e
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C2735
'keyword' keyword is not permitted in formal parameter type specifier  
  
 The keyword is invalid in this context.  
  
 The following sample generates C2735:  
  
```  
// C2735.cpp  
void f(inline int){}   // C2735  
```