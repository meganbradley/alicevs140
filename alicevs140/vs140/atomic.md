---
title: "atomic"
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
ms.topic: article
ms.assetid: 275e0338-cf2f-4525-97b5-696250000df7
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# atomic
Specifies that a memory location that will be updated atomically.  
  
## Syntax  
  
```  
#pragma omp atomic  
   expression  
```  
  
#### Parameters  
 `expression`  
 The statement containing the lvalue whose memory location you want to protect against multiple writes. For more information about legal expression forms, see the OpenMP specification.  
  
## Remarks  
 The `atomic` directive supports no OpenMP clauses.  
  
 For more information, see [2.6.4 atomic Construct](../vs140/2.6.4-atomic-Construct.md).  
  
## Example  
  
```  
// omp_atomic.cpp  
// compile with: /openmp   
#include <stdio.h>  
#include <omp.h>  
  
#define MAX 10  
  
int main() {  
   int count = 0;  
   #pragma omp parallel num_threads(MAX)  
   {  
      #pragma omp atomic  
      count++;  
   }  
   printf_s("Number of threads: %d\n", count);  
}  
```  
  
 **Number of threads: 10**   
## See Also  
 [OpenMP](../vs140/OpenMP-in-Visual-C--.md)