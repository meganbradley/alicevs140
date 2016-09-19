---
title: "Compiler Warning (level 1) C4600"
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
ms.assetid: f023a2a1-7fc4-463f-a434-dc93fcd3f4e9
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (level 1) C4600
\#pragma 'macro name' : expected a valid non-empty string  
  
 You cannot specify an empty string when you push or pop a macro name with either the [pop_macro](../vs140/pop_macro.md) or [push_macro](../vs140/push_macro.md).  
  
 The following sample generates C4600:  
  
```  
// C4600.cpp  
// compile with: /W1  
int main()  
{  
   #pragma push_macro("")   // C4600 passing an empty string  
}  
```