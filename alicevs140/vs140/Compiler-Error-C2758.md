---
title: "Compiler Error C2758"
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
ms.assetid: 1d273034-194c-4926-9869-142d1b219cbe
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C2758
'member': a member of reference type must be initialized  
  
 Compiler error C2758 is caused when the constructor does not initialize a member of reference type in an initializer list. The compiler leaves the member undefined. Reference member variables must initialized when declared or be given a value in the initialization list of the constructor.  
  
 The following sample generates C2758:  
  
```  
// C2758.cpp  
// Compile by using: cl /W3 /c C2758.cpp  
struct A {  
   const int i;  
  
   A(int n) { };   // C2758  
   // try the following line instead  
   // A(int n) : i{n} {};  
};  
```