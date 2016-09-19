---
title: "A.10   Specifying Sequential Ordering"
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
ms.assetid: 5c65a9b1-0fc5-4cad-a5a9-9ce10b25d25c
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# A.10   Specifying Sequential Ordering
Ordered sections ([Section 2.6.6](../vs140/2.6.6-ordered-Construct.md) on page 22) are useful for sequentially ordering the output from work that is done in parallel. The following program prints out the indexes in sequential order:  
  
```  
#pragma omp for ordered schedule(dynamic)  
    for (i=lb; i<ub; i+=st)  
        work(i);  
void work(int k)  
{  
    #pragma omp ordered  
        printf_s(" %d", k);  
}  
```