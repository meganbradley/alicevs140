---
title: "Compiler Error C2192"
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
ms.assetid: a147197e-e72d-4620-939b-f9e08d7c7c12
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C2192
parameter 'number' declaration different  
  
 A C function was declared a second time with a different parameter list. C does not support overloaded functions.  
  
 The following sample generates C2192:  
  
```  
// C2192.c  
// compile with: /Za /c  
void func( float, int );  
void func( int, float );   // C2192, different parameter list  
void func2( int, float );   // OK  
```