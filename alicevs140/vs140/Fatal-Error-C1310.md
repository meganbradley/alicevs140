---
title: "Fatal Error C1310"
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
ms.assetid: ac48aa51-8023-42fe-b844-3f8bf228fbef
caps.latest.revision: 7
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Fatal Error C1310
profile guided optimizations are not available with OpenMP  
  
 You will not be able to link with [/LTCG:PGI](../vs140/-LTCG--Link-time-Code-Generation-.md) any module that was compiled with [/GL](../Topic/-GL%20\(Whole%20Program%20Optimization\).md).  
  
 The following sample generates C1310:  
  
```  
// C1310.cpp  
// compile with: /openmp /GL /link /LTCG:PGI  
// C1310 expected  
int main()  
{  
   int i = 0, j = 10;  
  
   #pragma omp parallel  
   {  
      #pragma omp for  
      for (i = 0; i < 0; i++)   
         --j;  
   }  
}  
```