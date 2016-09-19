---
title: "Compiler Error C2264"
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
ms.assetid: 158b72cc-cee9-4a08-bd79-b7a5955345a8
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C2264
'function' : error in function definition or declaration; function not called  
  
 The function cannot be called due to an incorrect definition or declaration.  
  
 The following sample generates C2264:  
  
```  
// C2264.cpp  
struct C {  
   // Delete the following line to resolve.  
   operator int(int = 0){}   // incorrect declaration  
};  
  
struct D {  
   operator int(){return 0;}   // OK  
};  
  
int main() {  
   int i;  
  
   C c;  
   i = c;   // C2264  
  
   D d;  
   i = d;   // OK  
}  
```