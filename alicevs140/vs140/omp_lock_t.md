---
title: "omp_lock_t"
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
ms.assetid: 51b80629-4ffc-4b8a-95c7-1af048f1f286
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# omp_lock_t
A type that holds the status of a lock, whether the lock is available or if a thread owns a lock.  
  
 The following functions use **omp_lock_t**:  
  
-   [omp_init_lock](../vs140/omp_init_lock.md)  
  
-   [omp_destroy_lock](../vs140/omp_destroy_lock.md)  
  
-   [omp_set_lock](../vs140/omp_set_lock.md)  
  
-   [omp_unset_lock](../vs140/omp_unset_lock.md)  
  
-   [omp_test_lock](../vs140/omp_test_lock.md)  
  
 For more information, see [3.2 Lock Functions](../vs140/3.2-Lock-Functions.md).  
  
## Example  
 See [omp_init_lock](../vs140/omp_init_lock.md) for an example of using **omp_lock_t**.  
  
## See Also  
 [Data Types](../vs140/OpenMP-Data-Types.md)