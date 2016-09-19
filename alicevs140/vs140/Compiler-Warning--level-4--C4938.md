---
title: "Compiler Warning (level 4) C4938"
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
ms.assetid: 6acac81a-9d23-465e-b700-ed4b6e8edcd0
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (level 4) C4938
'var' : Floating point reduction variable may cause inconsistent results under /fp:strict or #pragma fenv_access  
  
 You should not use [/fp:strict](../Topic/-fp%20\(Specify%20Floating-Point%20Behavior\).md) or [fenv_access](../vs140/fenv_access.md) with OpenMP floating-point reductions, because the sum is computed in a different order. Thus, results can differ from the results without /openmp.  
  
 The following sample generates C4938:  
  
```  
// C4938.cpp  
// compile with: /openmp /W4 /fp:strict /c  
// #pragma fenv_access(on)  
extern double *a;   
  
double test(int first, int last) {   
   double sum = 0.0;   
   #pragma omp parallel for reduction(+: sum)   // C4938  
   for (int i = first ; i <= last ; ++i)   
      sum += a[i];   
   return sum;   
}  
```  
  
 Without explicit parallelization, the sum is computed as follows:  
  
```  
sum = a[first] + a[first + 1] + ... + a[last];   
```  
  
 With explicit parallelization (and two threads), the sum is computed as follows:  
  
```  
sum1 = a[first] + ... a[first + last / 2];   
sum2 = a[(first + last / 2) + 1] + ... a[last];   
sum = sum1 + sum2;  
```