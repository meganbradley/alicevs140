---
title: "Compiler Warning (level 1) C4558"
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
ms.assetid: 52bb0324-7bec-468c-b35b-13a08d38e578
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (level 1) C4558
value of operand 'value' is out of range 'lowerbound - upperbound'  
  
 The value passed to an assembly language instruction is out of the range specified for the parameter. The value will be truncated.  
  
 The following sample generates C4558:  
  
```  
// C4558.cpp  
// compile with: /W1  
// processor: x86  
void asm_test() {  
   __asm pinsrw   mm1, eax, 8;   // C4558  
}  
  
int main() {  
}  
```