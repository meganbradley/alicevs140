---
title: "A.18   Nested for Directives"
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
ms.assetid: ae2b2e0b-ec94-43f8-928c-6d621b51f0df
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# A.18   Nested for Directives
The following example of `for` directive nesting ([Section 2.9](../vs140/2.9-Directive-Nesting.md) on page 33) is compliant because the inner and outer `for` directives bind to different parallel regions:  
  
```  
#pragma omp parallel default(shared)  
{  
    #pragma omp for  
        for (i=0; i<n; i++)   
        {  
            #pragma omp parallel shared(i, n)  
            {  
                #pragma omp for  
                    for (j=0; j<n; j++)  
                        work(i, j);  
            }  
        }  
}  
```  
  
 A following variation of the preceding example is also compliant:  
  
```  
#pragma omp parallel default(shared)  
{  
    #pragma omp for  
        for (i=0; i<n; i++)  
            work1(i, n);  
}  
  
void work1(int i, int n)  
{  
    int j;  
    #pragma omp parallel default(shared)  
    {  
        #pragma omp for  
            for (j=0; j<n; j++)  
                work2(i, j);  
    }  
    return;  
}  
```