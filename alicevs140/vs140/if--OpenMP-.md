---
title: "if (OpenMP)"
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
ms.assetid: db5940b6-2414-4bf8-934d-3edd8393c0f8
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# if (OpenMP)
Specifies whether a loop should be executed in parallel or in serial.  
  
## Syntax  
  
```  
if(expression)  
```  
  
## Remarks  
 where,  
  
 `expression`  
 An integral expression that, if it evaluates to true (nonzero), causes the code in the parallel region to execute in parallel. If the expression evaluates to false (zero), the parallel region is executed in serial (by a single thread).  
  
## Remarks  
 `if` applies to the following directives:  
  
-   [parallel](../vs140/parallel.md)  
  
-   [for](../vs140/for--OpenMP-.md)  
  
-   [sections](../vs140/sections--OpenMP-.md)  
  
 For more information, see [2.3 parallel Construct](../vs140/2.3-parallel-Construct.md).  
  
## Example  
  
```  
// omp_if.cpp  
// compile with: /openmp  
#include <stdio.h>  
#include <omp.h>  
  
void test(int val)  
{  
    #pragma omp parallel if (val)  
    if (omp_in_parallel())  
    {  
        #pragma omp single  
        printf_s("val = %d, parallelized with %d threads\n",  
                 val, omp_get_num_threads());  
    }  
    else  
    {  
        printf_s("val = %d, serialized\n", val);  
    }  
}  
  
int main( )  
{  
    omp_set_num_threads(2);  
    test(0);  
    test(2);  
}  
```  
  
 **val = 0, serialized**  
**val = 2, parallelized with 2 threads**   
## See Also  
 [Clauses](../vs140/OpenMP-Clauses.md)