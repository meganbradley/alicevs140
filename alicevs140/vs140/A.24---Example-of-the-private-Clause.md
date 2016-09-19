---
title: "A.24   Example of the private Clause"
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
ms.assetid: f90a5b49-81ff-4746-ae03-37bbd33f6c08
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# A.24   Example of the private Clause
The `private` clause ([Section 2.7.2.1](../vs140/2.7.2.1-private.md) on page 25) of a parallel region is only in effect for the lexical extent of the region, not for the dynamic extent of the region.  Therefore, in the example that follows, any uses of the variable *a* within the `for` loop in the routine *f* refers to a private copy of *a*, while a usage in routine *g* refers to the global *a*.  
  
```  
int a;  
  
void f(int n)   
{  
    a = 0;  
  
    #pragma omp parallel for private(a)  
    for (int i=1; i<n; i++)   
    {  
        a = i;  
        g(i, n);  
        d(a);     // Private copy of "a"  
        ...  
    }  
    ...  
  
void g(int k, int n)   
{  
    h(k,a); // The global "a", not the private "a" in f  
}  
```