---
title: "Compiler Error C2425"
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
ms.assetid: 0ce59404-9aff-4e01-aa8d-27d23e92eb30
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C2425
'token' :non-constant expression in 'context'  
  
 The token forms part of a non-constant expression in this context.  
  
 To fix this issue, replace the token with a constant literal or with a calculation.  
  
 The following sample generates C2425:  
  
```  
// C2425.cpp  
// processor: x86  
int main() {  
   int i = 3;  
   __asm {  
      mov eax, [ebp - i]   // C2425  
      mov eax, [ebp - 3]   // OK  
   }  
}  
```