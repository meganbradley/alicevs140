---
title: "Compiler Error C3032"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 6a92bd8e-319f-4a99-aef4-a9021f6f9928
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C3032
'var' : variable in 'clause' clause cannot have incomplete type 'type'  
  
 Types passed to certain clauses must be fully visible to the compiler.  
  
 The following sample generates C3032:  
  
```  
// C3032.cpp  
// compile with: /openmp /link vcomps.lib  
#include "omp.h"  
  
struct Incomplete;  
extern struct Incomplete inc;  
  
int main() {  
   int i = 9;  
   #pragma omp parallel private(inc)   // C3032  
      ;  
  
   #pragma omp parallel private(i)     // OK  
      ;  
  
}  
```