---
title: "A.17   Using Nestable Locks"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 8ef386ed-ddc4-4d40-80aa-cc39f0fb5e4b
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# A.17   Using Nestable Locks
The following example (for [Section 3.2](../vs140/3.2-Lock-Functions.md) on page 41) demonstrates how a nestable lock can be used to synchronize updates both to a whole structure and to one of its members.  
  
```  
#include <omp.h>  
typedef struct {int a,b; omp_nest_lock_t lck;} pair;  
  
void incr_a(pair *p, int a)  
{  
    // Called only from incr_pair, no need to lock.  
    p->a += a;  
}  
  
void incr_b(pair *p, int b)  
{  
    // Called both from incr_pair and elsewhere,  
    // so need a nestable lock.  
  
    omp_set_nest_lock(&p->lck);  
    p->b += b;  
    omp_unset_nest_lock(&p->lck);  
}  
  
void incr_pair(pair *p, int a, int b)  
{  
    omp_set_nest_lock(&p->lck);  
    incr_a(p, a);  
    incr_b(p, b);  
    omp_unset_nest_lock(&p->lck);  
}  
  
void f(pair *p)  
{  
    extern int work1(), work2(), work3();  
    #pragma omp parallel sections  
    {  
        #pragma omp section  
            incr_pair(p, work1(), work2());  
        #pragma omp section  
            incr_b(p, work3());  
    }  
}  
```