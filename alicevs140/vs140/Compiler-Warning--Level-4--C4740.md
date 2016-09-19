---
title: "Compiler Warning (Level 4) C4740"
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
ms.assetid: 85528969-966a-44b4-8a2f-971704c64477
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (Level 4) C4740
flow in or out of inline asm code suppresses global optimization  
  
 When there is a jump in to or out of an `asm` block, global optimizations are disabled for that function.  
  
 The following sample generates C4740:  
  
```  
// C4740.cpp  
// compile with: /O2 /W4  
// processor: x86  
int main() {  
   __asm jmp tester  
   tester:;  
}  
```