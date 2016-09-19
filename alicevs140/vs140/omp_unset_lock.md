---
title: "omp_unset_lock"
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
ms.assetid: 68fcb728-040b-4bad-979e-aaecb9097a4e
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# omp_unset_lock
Releases a lock.  
  
## Syntax  
  
```  
void omp_unset_lock(  
   omp_lock_t *lock  
);  
```  
  
## Remarks  
 where,  
  
 `lock`  
 A variable of type [omp_lock_t](../vs140/omp_lock_t.md) that was initialized with [omp_init_lock](../vs140/omp_init_lock.md), owned by the thread and executing in the function.  
  
## Remarks  
 For more information, see [3.2.4 omp_unset_lock and omp_unset_nest_lock Functions](../vs140/3.2.4-omp_unset_lock-and-omp_unset_nest_lock-Functions.md).  
  
## Example  
 See [omp_init_lock](../vs140/omp_init_lock.md) for an example of using `omp_unset_lock`.  
  
## See Also  
 [Functions](../vs140/OpenMP-Functions.md)