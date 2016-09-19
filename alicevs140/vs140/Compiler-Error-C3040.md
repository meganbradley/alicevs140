---
title: "Compiler Error C3040"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 29e857ac-74f0-4ec6-becf-9026e38c160e
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C3040
'var' : type of variable in 'reduction' clause is incompatible with reduction operator 'operator'  
  
 A variable in a [reduction](../vs140/reduction.md) clause cannot be used with the reduction operator.  
  
 The following sample generates C3040:  
  
```  
// C3040.cpp  
// compile with: /openmp /c  
#include "omp.h"  
double d;  
  
int main() {  
   #pragma omp parallel reduction(&:d)   // C3040  
      ;  
  
   #pragma omp parallel reduction(-:d)  // OK  
      ;  
}  
```