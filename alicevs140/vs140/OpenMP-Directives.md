---
title: "OpenMP Directives"
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
ms.assetid: 0562c263-344c-466d-843e-de830d918940
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# OpenMP Directives
Provides links to directives used in the OpenMP API.  
  
 Visual C++ supports the following OpenMP directives:  
  
|Directive|Description|  
|---------------|-----------------|  
|[atomic](../vs140/atomic.md)|Specifies that a memory location that will be updated atomically.|  
|[barrier](../vs140/barrier.md)|Synchronizes all threads in a team; all threads pause at the barrier, until all threads execute the barrier.|  
|[critical](../vs140/critical.md)|Specifies that code is only executed on one thread at a time.|  
|[flush](../vs140/flush--OpenMP-.md)|Specifies that all threads have the same view of memory for all shared objects.|  
|[for](../vs140/for--OpenMP-.md)|Causes the work done in a for loop inside a parallel region to be divided among threads.|  
|[master](../vs140/master.md)|Specifies that only the master threadshould execute a section of the program.|  
|[ordered](../vs140/ordered--OpenMP-Directives-.md)|Specifies that code under a parallelized for loop should be executed like a sequential loop.|  
|[parallel](../vs140/parallel.md)|Defines a parallel region, which is code that will be executed by multiple threads in parallel.|  
|[sections](../vs140/sections--OpenMP-.md)|Identifies code sections to be divided among all threads.|  
|[single](../vs140/single.md)|Lets you specify that a section of code should be executed on a single thread, not necessarily the master thread.|  
|[threadprivate](../vs140/threadprivate.md)|Specifies that a variable is private to a thread.|  
  
## See Also  
 [OpenMP](../vs140/OpenMP-in-Visual-C--.md)   
 [Clauses](../vs140/OpenMP-Clauses.md)