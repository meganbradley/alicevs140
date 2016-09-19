---
title: "omp_set_nested"
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
ms.assetid: fa1cb08c-7b8b-42c9-8654-2c33dcffb5b6
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# omp_set_nested
Enables nested parallelism.  
  
## Syntax  
  
```  
void omp_set_nested(  
   int val  
);  
```  
  
## Remarks  
 where,  
  
 `val`  
 If nonzero, enables nested parallelism. If zero, disables nested parallelism.  
  
## Remarks  
 OMP nested parallelism can be turned on with `omp_set_nested`, or by setting the [OMP_NESTED](../vs140/OMP_NESTED.md) environment variable.  
  
 The setting for `omp_set_nested` will override the setting of the `OMP_NESTED` environment variable.  
  
 When enabled, the environment variable can break an otherwise operational program because the number of threads increases exponentially when nesting parallel regions.  For example a function that recurses 6 times with the number of OMP threads set to 4 requires 4,096 (4 to the power of 6) threads  In general, the performance of your application will degrade if the number of thread exceeds the number of processors. One exception to this would be I/O bound applications.  
  
 Use [omp_get_nested](../vs140/omp_get_nested.md) to display the current setting of `omp_set_nested`.  
  
 For more information, see [3.1.9 omp_set_nested Function](../vs140/3.1.9-omp_set_nested-Function.md).  
  
## Example  
  
```  
// omp_set_nested.cpp  
// compile with: /openmp  
#include <stdio.h>  
#include <omp.h>  
  
int main( )   
{  
    omp_set_nested(1);  
    omp_set_num_threads(4);  
    printf_s("%d\n", omp_get_nested( ));  
    #pragma omp parallel  
        #pragma omp master  
        {  
            printf_s("%d\n", omp_get_nested( ));  
        }  
}  
```  
  
 **1**  
**1**   
## See Also  
 [Functions](../vs140/OpenMP-Functions.md)