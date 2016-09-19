---
title: "Compiler Error C2483"
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
ms.assetid: 5762b325-914b-442d-a604-e4617ba04038
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C2483
'identifier' : object with constructor or destructor cannot be declared 'thread'  
  
 Variables declared with the `thread` attribute cannot be initialized with a constructor or other expression that requires run-time evaluation. A static expression is required to initialize `thread` data.  
  
## Example  
 The following sample generates C2483.  
  
```  
// C2483.cpp  
// compile with: /c  
__declspec(thread) struct A {  
   A(){}  
   ~A(){}  
} aa;   // C2483 error  
  
__declspec(thread) struct B {} b;   // OK  
```  
  
## See Also  
 [thread](../vs140/thread.md)