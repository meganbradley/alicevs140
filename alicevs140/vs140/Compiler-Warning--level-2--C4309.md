---
title: "Compiler Warning (level 2) C4309"
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
ms.assetid: cb3f41ef-fd8a-4def-baa1-924e751fca68
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (level 2) C4309
'conversion' : truncation of constant value  
  
 The type conversion causes a constant to exceed the space allocated for it. You may need to use a larger type for the constant.  
  
 The following sample generates C4309:  
  
```  
// C4309.cpp  
// compile with: /W2  
int main()  
{  
   char c = 128;   // C4309  
}  
```