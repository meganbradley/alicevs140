---
title: "Compiler Error C2564"
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
ms.assetid: c27e7514-549a-4b78-bdcc-fa8ce8e59159
caps.latest.revision: 9
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C2564
'type' : a function-style conversion to a built-in type can only take one argument  
  
 Function-style type casts of built-in types take a single argument.  
  
 The following sample generates C2564:  
  
```  
// C2564.cpp  
void g(float f, double d) {  
   int j = int(f, d);   // C2564  
}  
```