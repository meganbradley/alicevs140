---
title: "Compiler Error C2381"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: error-reference
ms.assetid: cc765f67-64ac-406f-93ef-ae7d548d58d7
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C2381
'function' : redefinition; __declspec(noreturn) differs  
  
 A function was declared and then defined but the definition used the [noreturn](../vs140/noreturn.md) `__declspec` modifier. The use of `noreturn` constitutes a redefinition of the function; the declaration and definition need to agree on the use of `noreturn`.  
  
 The following sample generates C2381:  
  
```  
// C2381.cpp  
// compile with: /c  
void f1();  
void __declspec(noreturn) f1() {}   // C2381  
void __declspec(noreturn) f2() {}   // OK  
```