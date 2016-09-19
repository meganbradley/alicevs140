---
title: "Compiler Error C2705"
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
ms.assetid: 29249ea3-4ea7-4105-944b-bdb83e8d6852
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C2705
'label' : illegal jump into 'exception handler block' scope  
  
 Execution jumps to a label within a `try`/`catch`, `__try`/`__except`, `__try`/`__finally` block. For more information, see [Exception Handling](../vs140/Exception-Handling-in-Visual-C--.md).  
  
 The following sample generates C2705:  
  
```  
// C2705.cpp  
int main() {  
goto trouble;  
   __try {  
      trouble: ;   // C2705  
   }  
   __finally {}  
  
   // try the following line instead  
   // trouble: ;  
}  
```