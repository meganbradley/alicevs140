---
title: "A.1   Executing a Simple Loop in Parallel"
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
ms.assetid: b8aaacae-b20d-4b16-a540-54ccbf09582b
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# A.1   Executing a Simple Loop in Parallel
The following example demonstrates how to parallelize a simple loop using the `parallel for` directive ([Section 2.5.1](../vs140/2.5.1-parallel-for-Construct.md) on page 16). The loop iteration variable is private by default, so it is not necessary to specify it explicitly in a private clause.  
  
```  
#pragma omp parallel for  
    for (i=1; i<n; i++)  
        b[i] = (a[i] + a[i-1]) / 2.0;  
```