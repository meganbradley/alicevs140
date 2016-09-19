---
title: "Compiler Error C2191"
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
ms.assetid: 051b8350-e5de-4f51-ab6e-96d32366bcef
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C2191
second parameter list longer than first  
  
 A C function was declared a second time with a longer parameter list. C does not support overloaded functions.  
  
## Example  
 The following sample generates C2191:  
  
```  
// C2191.c  
// compile with: /Za /c  
void func( int );  
void func( int, float );   // C2191 different parameter list  
void func2( int, float );   // OK  
```