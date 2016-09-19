---
title: "num_threads"
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
ms.assetid: 09a56fc8-25c7-43e4-bbb5-71cb955d0b93
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# num_threads
Sets the number of threads in a thread team.  
  
## Syntax  
  
```  
num_threads(num)  
```  
  
## Remarks  
 where,  
  
 `num`  
 The number of threads  
  
## Remarks  
 The `num_threads` clause has the same functionality as the [omp_set_num_threads](../vs140/omp_set_num_threads.md) function.  
  
 `num_threads` applies to the following directives:  
  
-   [parallel](../vs140/parallel.md)  
  
-   [for](../vs140/for--OpenMP-.md)  
  
-   [sections](../vs140/sections--OpenMP-.md)  
  
 For more information, see [2.3 parallel Construct](../vs140/2.3-parallel-Construct.md).  
  
## Example  
 See [parallel](../vs140/parallel.md) for an example of using `num_threads` clause.  
  
## See Also  
 [Clauses](../vs140/OpenMP-Clauses.md)