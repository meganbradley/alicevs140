---
title: "omp_set_dynamic"
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
ms.assetid: 3845faf2-a0ca-45a5-ae70-2a7a6164f1e8
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# omp_set_dynamic
Indicates that the number of threads available in subsequent parallel region can be adjusted by the run time.  
  
## Syntax  
  
```  
void omp_set_dynamic(  
   int val  
);  
```  
  
## Remarks  
 where,  
  
 `val`  
 A value that indicates if the number of threads available in subsequent parallel region can be adjusted by the runtime.  If nonzero, the runtime can adjust the number of threads, if zero, the runtime will not dynamically adjust the number of threads.  
  
## Remarks  
 The number of threads will never exceed the value set by [omp_set_num_threads](../vs140/omp_set_num_threads.md) or by [OMP_NUM_THREADS](../vs140/OMP_NUM_THREADS.md).  
  
 Use [omp_get_dynamic](../vs140/omp_get_dynamic.md) to display the current setting of `omp_set_dynamic`.  
  
 The setting for `omp_set_dynamic` will override the setting of the [OMP_DYNAMIC](../vs140/OMP_DYNAMIC.md) environment variable.  
  
 For more information, see [3.1.7 omp_set_dynamic Function](../vs140/3.1.7-omp_set_dynamic-Function.md).  
  
## Example  
  
```  
// omp_set_dynamic.cpp  
// compile with: /openmp  
#include <stdio.h>  
#include <omp.h>  
  
int main()   
{  
    omp_set_dynamic(9);  
    omp_set_num_threads(4);  
    printf_s("%d\n", omp_get_dynamic( ));  
    #pragma omp parallel  
        #pragma omp master  
        {  
            printf_s("%d\n", omp_get_dynamic( ));  
        }  
}  
```  
  
 **1**  
**1**   
## See Also  
 [Functions](../vs140/OpenMP-Functions.md)