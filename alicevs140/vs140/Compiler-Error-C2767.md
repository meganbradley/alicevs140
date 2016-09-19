---
title: "Compiler Error C2767"
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
ms.assetid: e8f84178-a160-4d71-a236-07e4fcc11e96
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C2767
managed or WinRTarray dimension mismatch : expected N argument(s) - M provided  
  
 A managed or WinRT array declaration was ill formed. For more information, see [array](../vs140/Arrays--C---Component-Extensions-.md).  
  
 The following sample generates C2767 and shows how to fix it:  
  
```  
// C2767.cpp  
// compile with: /clr  
int main() {  
   array<int> ^p1 = new array<int>(2,3); // C2767  
   array<int> ^p2 = new array<int>(2);   // OK  
}  
```