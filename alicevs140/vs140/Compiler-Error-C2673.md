---
title: "Compiler Error C2673"
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
ms.assetid: 780230c0-619b-4a78-b01d-ff5886306741
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C2673
'function' : global functions do not have 'this' pointers  
  
 A global function tried to access `this`.  
  
 The following sample generates C2673:  
  
```  
// C2673.cpp  
int main() {  
   this = 0;   // C2673  
}  
```