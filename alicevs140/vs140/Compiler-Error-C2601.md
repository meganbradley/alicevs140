---
title: "Compiler Error C2601"
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
ms.assetid: 88275582-5f37-45d7-807d-05f06ba00965
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C2601
'function' : local function definitions are illegal  
  
 Code tries to define a function within a function.  
  
 Or, there may be an extra brace in your source code before the location of the C2601 error.  
  
 The following sample generates C2601:  
  
```  
// C2601.cpp  
int main() {  
   int i = 0;  
  
   void funcname(int j) {   // C2601  
      j++;  
   }  
}  
```