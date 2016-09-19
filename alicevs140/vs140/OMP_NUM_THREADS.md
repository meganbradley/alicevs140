---
title: "OMP_NUM_THREADS"
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
ms.assetid: 4b558124-1387-4c30-a6a5-ff5345a9ced6
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# OMP_NUM_THREADS
Sets the maximum number of threads in the parallel region, unless overridden by [omp_set_num_threads](../vs140/omp_set_num_threads.md) or [num_threads](../vs140/num_threads.md).  
  
## Syntax  
  
```  
set OMP_NUM_THREADS[=num]  
```  
  
## Remarks  
 where,  
  
 `num`  
 The maximum number of threads you want in the parallel region, up to 64 in the Visual C++ implementation.  
  
## Remarks  
 The **OMP_NUM_THREADS** environment variable can be overridden by the [omp_set_num_threads](../vs140/omp_set_num_threads.md) function or by [num_threads](../vs140/num_threads.md).  
  
 The default value of `num` in the Visual C++ implementation of the OpenMP standard is the number of virtual processors, including hyperthreading CPUs.  
  
 For more information, see [4.2 OMP_NUM_THREADS](../vs140/4.2-OMP_NUM_THREADS.md).  
  
## Example  
 The following command sets the **OMP_NUM_THREADS** environment variable to 16:  
  
```  
set OMP_NUM_THREADS=16  
```  
  
 The following command displays the current setting of the **OMP_NUM_THREADS** environment variable:  
  
```  
set OMP_NUM_THREADS  
```  
  
## See Also  
 [Environment Variables](../vs140/OpenMP-Environment-Variables.md)