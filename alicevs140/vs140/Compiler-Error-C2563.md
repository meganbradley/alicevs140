---
title: "Compiler Error C2563"
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
ms.assetid: 54abba68-6458-4ca5-894d-3babdb7b3552
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C2563
mismatch in formal parameter list  
  
 The formal parameter list of a function (or a pointer to a function) does not match those of another function (or pointer to a member function). As a result, the assignment of functions or pointers cannot be made.  
  
 The following sample generates C2563:  
  
```  
// C2563.cpp  
void func( int );  
void func( int, int );  
int main() {  
   void *fp();  
   fp = func;   // C2563  
}  
```