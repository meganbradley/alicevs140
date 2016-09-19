---
title: "A.20   Binding of barrier Directives"
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
ms.assetid: a3fdcc26-6873-429b-998e-de451401483b
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# A.20   Binding of barrier Directives
The directive binding rules call for a **barrier** directive to bind to the closest enclosing `parallel` directive. For more information on directive binding, see [Section 2.8](../vs140/2.8-Directive-Binding.md) on page 32.  
  
 In the following example, the call from *main* to *sub2* is compliant because the **barrier** (in *sub3*) binds to the parallel region in *sub2*. The call from *main* to *sub1* is compliant because the **barrier** binds to the parallel region in subroutine *sub2*.  The call from *main* to *sub3* is compliant because the **barrier** does not bind to any parallel region and is ignored. Also note that the **barrier** only synchronizes the team of threads in the enclosing parallel region and not all the threads created in *sub1*.  
  
```  
int main()  
{  
    sub1(2);  
    sub2(2);  
    sub3(2);  
}  
  
void sub1(int n)  
{  
    int i;  
    #pragma omp parallel private(i) shared(n)  
    {  
        #pragma omp for  
        for (i=0; i<n; i++)  
            sub2(i);  
    }  
}  
  
void sub2(int k)  
{  
     #pragma omp parallel shared(k)  
     sub3(k);  
}  
  
void sub3(int n)  
{  
    work(n);  
    #pragma omp barrier  
    work(n);  
}  
```