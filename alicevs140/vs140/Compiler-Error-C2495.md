---
title: "Compiler Error C2495"
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
ms.assetid: bb7066fe-3549-4901-97e4-157f3c04dd57
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C2495
'identifier' : 'nothrow' can only be applied to function declarations or definitions  
  
 The [nothrow](../vs140/nothrow--C---.md) extended attribute can be applied to function declarations or definitions only.  
  
 The following sample generates C2495:  
  
```  
// C2495.cpp  
// compile with: /c  
__declspec(nothrow) class X {   // C2495  
   int m_data;  
} x;  
  
__declspec(nothrow) void test();   // OK  
```