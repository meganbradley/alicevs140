---
title: "nowait"
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
ms.assetid: 8a74265d-879c-46cf-8071-a1084f24f16e
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# nowait
Overrides the barrier implicit in a directive.  
  
## Syntax  
  
```  
nowait  
```  
  
## Remarks  
 `nowait` applies to the following directives:  
  
-   [for](../vs140/for--OpenMP-.md)  
  
-   [sections](../vs140/sections--OpenMP-.md)  
  
-   [single](../vs140/single.md)  
  
 For more information, see [2.4.1 for Construct](../vs140/2.4.1-for-Construct.md), [2.4.2 sections Construct](../vs140/2.4.2-sections-Construct.md), and [2.4.3 single Construct](../vs140/2.4.3-single-Construct.md).  
  
## Example  
  
```  
// omp_nowait.cpp  
// compile with: /openmp /c  
#include <stdio.h>  
  
#define SIZE 5  
  
void test(int *a, int *b, int *c, int size)   
{  
    int i;  
    #pragma omp parallel  
    {  
        #pragma omp for nowait  
        for (i = 0; i < size; i++)  
            b[i] = a[i] * a[i];  
  
        #pragma omp for nowait  
        for (i = 0; i < size; i++)  
            c[i] = a[i]/2;  
    }  
}  
  
int main( )   
{  
    int a[SIZE], b[SIZE], c[SIZE];  
    int i;  
  
    for (i=0; i<SIZE; i++)  
        a[i] = i;  
  
    test(a,b,c, SIZE);  
  
    for (i=0; i<SIZE; i++)  
        printf_s("%d, %d, %d\n", a[i], b[i], c[i]);  
}  
```  
  
 **0, 0, 0**  
**1, 1, 0**  
**2, 4, 1**  
**3, 9, 1**  
**4, 16, 2**   
## See Also  
 [Clauses](../vs140/OpenMP-Clauses.md)