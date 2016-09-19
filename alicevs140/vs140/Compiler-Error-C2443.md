---
title: "Compiler Error C2443"
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
ms.assetid: 315330d5-24bc-4193-a531-0642095be58f
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C2443
operand size conflict  
  
 The instruction requires operands to be the same size.  
  
 The following sample generates C2443:  
  
```  
// C2443.cpp  
// processor: x86  
short var;  
int main() {  
   __asm xchg ax,bl   // C2443  
   __asm mov al,red   // C2443  
   __asm mov al,BYTE PTR var   // OK  
}  
```