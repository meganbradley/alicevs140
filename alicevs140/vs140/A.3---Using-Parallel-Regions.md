---
title: "A.3   Using Parallel Regions"
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
ms.topic: article
ms.assetid: 575216a1-960a-47f7-9c82-7f660291fcfe
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# A.3   Using Parallel Regions
The `parallel` directive ([Section 2.3](../vs140/2.3-parallel-Construct.md) on page 8) can be used in coarse-grain parallel programs. In the following example, each thread in the parallel region decides what part of the global array `x` to work on, based on the thread number:  
  
```  
#pragma omp parallel shared(x, npoints) private(iam, np, ipoints)  
{  
    iam = omp_get_thread_num();  
    np =  omp_get_num_threads();  
    ipoints = npoints / np;  
    subdomain(x, iam, ipoints);  
}  
```