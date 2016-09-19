---
title: "Compiler Warning (level 4) C4212"
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
ms.assetid: df781ea1-182d-4f9f-9a31-55b6ce80c711
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (level 4) C4212
nonstandard extension used : function declaration used ellipsis  
  
 The function prototype has a variable number of arguments. The function definition does not.  
  
 The following sample generates C4212:  
  
```  
// C4212.c  
// compile with: /W4 /Ze /c  
void f(int , ...);  
void f(int i, int j) {}  
```