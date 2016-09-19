---
title: "parallel"
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
ms.assetid: b8e90073-e85b-4d39-8ed8-0364441794fb
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# parallel
Defines a parallel region, which is code that will be executed by multiple threads in parallel.  
  
## Syntax  
  
```  
#pragma omp parallel [clauses]  
{  
   code_block  
}  
```  
  
## Remarks  
 where,  
  
 `clause` (optional)  
 Zero or more clauses.  See the Remarks section for a list of the clauses supported by **parallel**.  
  
## Remarks  
 The **parallel** directive supports the following OpenMP clauses:  
  
-   [copyin](../vs140/copyin.md)  
  
-   [default](../vs140/default--OpenMP-.md)  
  
-   [firstprivate](../vs140/firstprivate.md)  
  
-   [if](../vs140/if--OpenMP-.md)  
  
-   [num_threads](../vs140/num_threads.md)  
  
-   [private](../vs140/private--OpenMP-.md)  
  
-   [reduction](../vs140/reduction.md)  
  
-   [shared](../vs140/shared--OpenMP-.md)  
  
 **parallel** can also be used with the [sections](../vs140/sections--OpenMP-.md) and [for](../vs140/for--OpenMP-.md) directives.  
  
 For more information, see [2.3 parallel Construct](../vs140/2.3-parallel-Construct.md).  
  
## Example  
 The following sample shows how to set the number of threads and define a parallel region. By default, the number of threads is equal to the number of logical processors on the machine. For example, if you have a machine with one physical processor that has hyperthreading enabled, it will have two logical processors and, therefore, two threads.  
  
```  
// omp_parallel.cpp  
// compile with: /openmp   
#include <stdio.h>  
#include <omp.h>  
  
int main() {  
   #pragma omp parallel num_threads(4)  
   {  
      int i = omp_get_thread_num();  
      printf_s("Hello from thread %d\n", i);  
   }  
}  
```  
  
 **Hello from thread 0**  
**Hello from thread 1**  
**Hello from thread 2**  
**Hello from thread 3**   
## Comment  
 Note that the order of output can vary on different machines.  
  
## See Also  
 [Directives](../vs140/OpenMP-Directives.md)