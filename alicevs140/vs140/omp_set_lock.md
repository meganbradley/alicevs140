---
title: "omp_set_lock"
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
ms.assetid: ded839cb-ca19-403f-8622-eb52ce512d31
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# omp_set_lock
Blocks thread execution until a lock is available.  
  
## Syntax  
  
```  
void omp_set_lock(  
   omp_lock_t *lock  
);  
```  
  
## Remarks  
 where,  
  
 `lock`  
 A variable of type [omp_lock_t](../vs140/omp_lock_t.md) that was initialized with [omp_init_lock](../vs140/omp_init_lock.md).  
  
## Remarks  
 For more information, see [3.2.3 omp_set_lock and omp_set_nest_lock Functions](../vs140/3.2.3-omp_set_lock-and-omp_set_nest_lock-Functions.md).  
  
## Examples  
 See [omp_init_lock](../vs140/omp_init_lock.md) for an example of using `omp_set_lock`.  
  
## See Also  
 [Functions](../vs140/OpenMP-Functions.md)