---
title: "OpenMP Clauses"
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
ms.assetid: 806e7d8f-b204-4e4c-a12c-273ab540a7ca
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# OpenMP Clauses
Provides links to clauses used in the OpenMP API.  
  
 Visual C++ supports the following OpenMP clauses:  
  
|Clause|Description|  
|------------|-----------------|  
|[copyin](../vs140/copyin.md)|Allows threads to access the master thread's value, for a [threadprivate](../vs140/threadprivate.md) variable.|  
|[copyprivate](../vs140/copyprivate.md)|Specifies that one or more variables should be shared among all threads.|  
|[default](../vs140/default--OpenMP-.md)|Specifies the behavior of unscoped variables in a parallel region.|  
|[firstprivate](../vs140/firstprivate.md)|Specifies that each thread should have its own instance of a variable, and that the variable should be initialized with the value of the variable, because it exists before the parallel construct.|  
|[if](../vs140/if--OpenMP-.md)|Specifies whether a loop should be executed in parallel or in serial.|  
|[lastprivate](../vs140/lastprivate.md)|Specifies that the enclosing context's version of the variable is set equal to the private version of whichever thread executes the final iteration (for-loop construct) or last section (#pragma sections).|  
|[nowait](../vs140/nowait.md)|Overrides the barrier implicit in a directive.|  
|[num_threads](../vs140/num_threads.md)|Sets the number of threads in a thread team.|  
|[ordered](../vs140/ordered--OpenMP-Clauses-.md)|Required on a parallel [for](../vs140/for--OpenMP-.md) statement if an [ordered](../vs140/ordered--OpenMP-Directives-.md) directive is to be used in the loop.|  
|[private](../vs140/private--OpenMP-.md)|Specifies that each thread should have its own instance of a variable.|  
|[reduction](../vs140/reduction.md)|Specifies that one or more variables that are private to each thread are the subject of a reduction operation at the end of the parallel region.|  
|[schedule](../vs140/schedule.md)|Applies to the [for](../vs140/for--OpenMP-.md) directive.|  
|[shared](../vs140/shared--OpenMP-.md)|Specifies that one or more variables should be shared among all threads.|  
  
## See Also  
 [OpenMP](../vs140/OpenMP-in-Visual-C--.md)   
 [Directives](../vs140/OpenMP-Directives.md)