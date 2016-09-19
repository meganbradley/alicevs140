---
title: "Compiler Error C2383"
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
ms.assetid: 6696221d-879c-477a-a0f3-a6edc15fd3d7
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C2383
'symbol' : default-arguments are not allowed on this symbol  
  
 The C++ compiler does not allow default arguments on pointers to functions.  
  
 This code was accepted by the previous version's compiler but now gives an error. For code that works in all versions of Visual C++, do not assign a default value to a pointer-to-function argument.  
  
 The following line generates C2383:  
  
```  
// C2383.cpp  
// compile with: /c   
void (*pf)(int = 0);   // C2383  
void (*pf)(int);   // OK  
```