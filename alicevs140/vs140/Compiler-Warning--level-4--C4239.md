---
title: "Compiler Warning (level 4) C4239"
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
ms.assetid: a23dc16a-649e-4870-9a24-275de1584fcd
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (level 4) C4239
nonstandard extension used : 'token' : conversion from 'type' to 'type'  
  
 This type conversion is not allowed by the C++ standard, but it is permitted here as an extension. This warning is always followed by at least one line of explanation describing the language rule being violated.  
  
## Example  
 The following sample generates C4239.  
  
```  
// C4239.cpp  
// compile with: /W4 /c  
struct C {  
   C() {}  
};  
  
void func(void) {  
   C & rC = C();   // C4239  
   const C & rC2 = C();   // OK  
   rC2;  
}  
```  
  
## Example  
 Conversion from integral type to enum type is not strictly allowed.  
  
 The following sample generates C4239.  
  
```  
// C4239b.cpp  
// compile with: /W4 /c  
enum E { value };   
struct S {   
   E e : 2;   
} s = { 5 };   // C4239   
// try the following line instead  
// } s = { (E)5 };  
```