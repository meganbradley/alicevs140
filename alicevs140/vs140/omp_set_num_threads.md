---
title: "omp_set_num_threads"
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
ms.assetid: dae0bf3f-cd7a-4413-89de-6149ac1f4fa7
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# omp_set_num_threads
Sets the number of threads in subsequent parallel regions, unless overridden by a [num_threads](../vs140/num_threads.md) clause.  
  
## Syntax  
  
```  
void omp_set_num_threads(  
   int num_threads  
);  
```  
  
## Remarks  
 where,  
  
 `num_threads`  
 The number of threads in the parallel region.  
  
## Remarks  
 For more information, see [3.1.1 omp_set_num_threads Function](../vs140/3.1.1-omp_set_num_threads-Function.md).  
  
## Example  
 See [omp_get_num_threads](../vs140/omp_get_num_threads.md) for an example of using `omp_set_num_threads`.  
  
## See Also  
 [Functions](../vs140/OpenMP-Functions.md)