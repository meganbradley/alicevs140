---
title: "Compiler Error C2461"
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
ms.assetid: e64ba651-f441-4fdb-b5cb-4209bbbe4db4
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C2461
'class' : constructor syntax missing formal parameters  
  
 The constructor for the class does not specify any formal parameters. The declaration of a constructor must specify a formal parameter. (The list can be null.)  
  
 Add a pair of parentheses after `class``::``class`.  
  
 The following sample generates C2461:  
  
```  
// C2461.cpp  
// compile with: /c  
class C {  
   C::C;   // C2461  
   C::C();   // OK  
};  
```