---
title: "ordered (OpenMP Directives)"
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
ms.assetid: e1aa703e-d07d-4f6a-9b2a-f4f25203d850
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ordered (OpenMP Directives)
Specifies that code under a parallelized for loop should be executed like a sequential loop.  
  
## Syntax  
  
```  
#pragma omp ordered  
   structured-block  
```  
  
## Remarks  
 The **ordered** directive must be within the dynamic extent of a [for](../vs140/for--OpenMP-.md) or **parallel for** construct with an **ordered** clause.  
  
 The **ordered** directive supports no OpenMP clauses.  
  
 For more information, see [2.6.6 ordered Construct](../vs140/2.6.6-ordered-Construct.md).  
  
## Example  
  
```  
// omp_ordered.cpp  
// compile with: /openmp   
#include <stdio.h>  
#include <omp.h>  
  
static float a[1000], b[1000], c[1000];  
  
void test(int first, int last)   
{  
    #pragma omp for schedule(static) ordered  
    for (int i = first; i <= last; ++i) {  
        // Do something here.  
        if (i % 2)   
        {  
            #pragma omp ordered   
            printf_s("test() iteration %d\n", i);  
        }  
    }  
}  
  
void test2(int iter)   
{  
    #pragma omp ordered  
    printf_s("test2() iteration %d\n", iter);  
}  
  
int main( )   
{  
    int i;  
    #pragma omp parallel  
    {  
        test(1, 8);  
        #pragma omp for ordered  
        for (i = 0 ; i < 5 ; i++)  
            test2(i);  
    }  
}  
```  
  
 **test() iteration 1**  
**test() iteration 3**  
**test() iteration 5**  
**test() iteration 7**  
**test2() iteration 0**  
**test2() iteration 1**  
**test2() iteration 2**  
**test2() iteration 3**  
**test2() iteration 4**   
## See Also  
 [Directives](../vs140/OpenMP-Directives.md)