---
title: "Compiler Error C2486"
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
ms.assetid: 436da349-6461-4e32-bfca-4f3e620108e2
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C2486
'__LOCAL_SIZE' only allowed in function with the 'naked' attribute  
  
 In inline assembly functions, the name `__LOCAL_SIZE` is reserved for functions declared with the [naked](../vs140/naked--C---.md) attribute.  
  
 The following sample generates C2486:  
  
```  
// C2486.cpp  
// processor: x86  
void __declspec(naked) f1() {  
   __asm {  
      mov   eax,   __LOCAL_SIZE  
   }  
}  
void f2() {  
   __asm {  
      mov   eax,   __LOCAL_SIZE   // C2486  
   }  
}  
```