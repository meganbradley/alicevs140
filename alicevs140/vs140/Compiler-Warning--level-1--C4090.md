---
title: "Compiler Warning (level 1) C4090"
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
ms.assetid: baad469d-23d4-45aa-ad9c-305b32d61e9a
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (level 1) C4090
'operation' : different 'modifier' qualifiers  
  
 A variable used in an operation is defined with a specified modifier that prevents it from being modified without detection by the compiler. The expression is compiled without modification.  
  
 This warning can be caused when a pointer to a **const** or `volatile` item is assigned to a pointer not declared as pointing to **const** or `volatile`.  
  
 This warning is issued for C programs. In a C++ program, the compiler issues an error: [C2440](../Topic/Compiler%20Error%20C2440.md).  
  
 The following sample generates C4090:  
  
```  
// C4090.c  
// compile with: /W1  
int *volatile *p;  
int *const *q;  
int **r;  
  
int main() {  
   p = q;   // C4090  
   p = r;  
   q = p;   // C4090  
   q = r;  
   r = p;   // C4090  
   r = q;   // C4090  
}  
```