---
title: "A.15   Determining the Number of Threads Used"
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
ms.assetid: 026bb59a-f668-40db-a7cb-69a1bae83d2d
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# A.15   Determining the Number of Threads Used
Consider the following incorrect example (for [Section 3.1.2](../vs140/3.1.2-omp_get_num_threads-Function.md) on page 37):  
  
```  
np = omp_get_num_threads(); // misplaced   
#pragma omp parallel for schedule(static)  
    for (i=0; i<np; i++)  
        work(i);  
```  
  
 The `omp_get_num_threads()` call returns 1 in the serial section of the code, so *np* will always be equal to 1 in the preceding example. To determine the number of threads that will be deployed for the parallel region, the call should be inside the parallel region.  
  
 The following example shows how to rewrite this program without including a query for the number of threads:  
  
```  
#pragma omp parallel private(i)  
{  
    i = omp_get_thread_num();  
    work(i);  
}  
```