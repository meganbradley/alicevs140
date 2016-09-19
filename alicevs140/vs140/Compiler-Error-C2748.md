---
title: "Compiler Error C2748"
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
ms.assetid: b63ac78b-a200-499c-afea-15af1a1e819e
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C2748
managed or WinRT array creation must have array size or array initializer  
  
 A managed or WinRT array was ill formed. For more information, see [array](../vs140/Arrays--C---Component-Extensions-.md).  
  
 The following sample generates C2748 and shows how to fix it:  
  
```  
// C2748.cpp  
// compile with: /clr  
int main() {  
   array<int> ^p1 = new array<int>();   // C2748  
   // try the following line instead  
   array<int> ^p2 = new array<int>(2);  
}  
```