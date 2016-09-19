---
title: "Compiler Error C2587"
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
ms.assetid: 7637a2c7-35d4-4b5a-a8f2-515a7bda98fd
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C2587
'identifier' : illegal use of local variable as default parameter  
  
 Local variables are not allowed as default parameters.  
  
 The following sample generates C2587:  
  
```  
// C2587.cpp  
// compile with: /c  
int i;  
void func() {  
   int j;  
   extern void func2( int k = j );  // C2587 -- local variable  
   extern void func3( int k = i );   // OK  
}  
```