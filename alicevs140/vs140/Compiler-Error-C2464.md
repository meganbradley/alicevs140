---
title: "Compiler Error C2464"
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
ms.assetid: ace953d6-b414-49ee-bfef-90578a8da00c
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C2464
'identifier' : cannot use 'new' to allocate a reference  
  
 A reference identifier was allocated with the `new` operator. References are not memory objects, so `new` cannot return a pointer to them. Use the standard variable declaration syntax to declare a reference.  
  
 The following sample generates C2464:  
  
```  
// C2464.cpp  
int main() {  
   new ( int& ir );   // C2464  
}  
```