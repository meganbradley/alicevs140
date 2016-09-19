---
title: "Compiler Error C2467"
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
ms.assetid: f9ead270-5d0b-41cc-bdcd-586a647c67a7
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C2467
illegal declaration of anonymous 'user-defined-type'  
  
 A nested user-defined type was declared. This is an error when compiling C source code with the ANSI compatibility option ([/Za](../Topic/-Za,%20-Ze%20\(Disable%20Language%20Extensions\).md)) enabled.  
  
 The following sample generates C2467:  
  
```  
//C2467.c  
// compile with: /Za   
int main() {  
   struct X {  
      union { int i; };   // C2467, nested declaration  
   };  
}  
```