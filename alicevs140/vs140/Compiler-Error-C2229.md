---
title: "Compiler Error C2229"
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
ms.assetid: 933c7cf2-a463-4e74-b0b4-59dedad987fb
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C2229
type 'identifier' has an illegal zero-sized array  
  
 A member of a structure or bit field contains a zero-sized array that is not the last member.  
  
 Because you can have a zero sized array as the last member of the struct, you must specify its size when you allocate the struct.  
  
 If the zero sized array is not the last member of the struct, the compiler can't calculate the offset for the remaining fields.  
  
 The following sample generates C2229:  
  
```  
// C2229.cpp  
struct S {  
   int a[0];  // C2229  zero-sized array  
   int b[1];  
};  
  
struct S2 {  
   int a;  
   int b[0];  
};  
  
int main() {  
   // allocate 7 elements for b field  
   S2* s2 = (S2*)new int[sizeof(S2) + 7*sizeof(int)];  
   s2->b[6] = 100;  
}  
```