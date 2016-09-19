---
title: "Compiler Error C2496"
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
ms.assetid: 9a25237d-5bbb-4112-98f3-29cd99d3f89f
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C2496
'identifier' : 'selectany' can only be applied to data items with external linkage  
  
 The [selectany](../vs140/selectany.md) attribute can be applied only to externally visible and global data items.  
  
 The following sample generates C2496:  
  
```  
// C2496.cpp  
// compile with: /c  
__declspec(selectany) int x1 = 1;  
const __declspec(selectany) int x2 = 2;   // C2496  
static __declspec(selectany) int x6 = 6;   // C2496  
  
extern const __declspec(selectany) int x3 = 3;  
  
__declspec(selectany) int x4;  
  
// dynamic initialization of x5  
int f();  
__declspec(selectany) int x5 = f();  
  
extern const int x7;  
// OK - redeclaration of x7 that is extern  
const __declspec(selectany) int x7 = 7;  
```