---
title: "Compiler Error C2462"
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
ms.assetid: a8601bf8-f5ce-41de-9117-e2632bd4996b
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C2462
'identifier' : cannot define a type in a 'new-expression'  
  
 You cannot define a type in the operand field of the `new` operator. Put the type definition in a separate statement.  
  
 The following sample generates C2462:  
  
```  
// C2462.cpp  
int main() {  
   new struct S { int i; };   // C2462  
}  
```