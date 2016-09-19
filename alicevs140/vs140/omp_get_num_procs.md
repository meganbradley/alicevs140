---
title: "omp_get_num_procs"
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
ms.assetid: 14a10b8f-e59b-4211-a292-687648c9f760
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# omp_get_num_procs
Returns the number of processors that are available when the function is called.  
  
## Syntax  
  
```  
int omp_get_num_procs();  
```  
  
## Remarks  
 For more information, see [3.1.5 omp_get_num_procs Function](../vs140/3.1.5-omp_get_num_procs-Function.md).  
  
## Example  
  
```  
// omp_get_num_procs.cpp  
// compile with: /openmp  
#include <stdio.h>  
#include <omp.h>  
  
int main( )   
{  
    printf_s("%d\n", omp_get_num_procs( ));  
    #pragma omp parallel  
        #pragma omp master  
        {  
            printf_s("%d\n", omp_get_num_procs( ));  
        }  
}  
```  
  
 **// Expect the following output when the example is run on a two-processor machine:**  
**2**  
**2**   
## See Also  
 [Functions](../vs140/OpenMP-Functions.md)