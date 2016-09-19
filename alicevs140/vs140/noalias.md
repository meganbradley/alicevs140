---
title: "noalias"
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
ms.topic: language-reference
ms.assetid: efafa8b0-7f39-4edc-a81e-d287ae882c9b
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# noalias
**Microsoft Specific**  
  
 `noalias` means that a function call does not modify or reference visible global state and only modifies the memory pointed to `directly` by pointer parameters (first-level indirections).  
  
 If a function is annotated as `noalias`, the optimizer can assume that, in addition to the parameters themselves, only first-level indirections of pointer parameters are referenced or modified inside the function. The visible global state is the set of all data that is not defined or referenced outside of the compilation scope, and their address is not taken. The compilation scope is all source files ([/LTCG (Link-time Code Generation)](../vs140/-LTCG--Link-time-Code-Generation-.md) builds) or a single source file (non-**/LTCG** build).  
  
## Example  
 The following sample demonstrates using `__declspec(restrict)` and `__declspec(noalias)`. Normally, memory returned from `malloc` is `restrict` and `noalias` because the CRT headers are decorated appropriately.  
  
 However, in this example, the pointers `mempool` and `memptr` are global so the compiler has no assurance that the memory is not subject to aliasing. Decorating the functions that return pointers with `__declspec(restrict)` tells the compiler that the memory pointed to by the return value is not aliased.  
  
 Decorating the function in the example that accesses memory with `__declspec(noalias)` tells the compiler that this function does not interfere with the global state except through the pointers in its parameter list.  
  
```  
// declspec_noalias.c   
#include <stdio.h>  
#include <stdlib.h>  
  
#define M 800  
#define N 600  
#define P 700  
  
float * mempool, * memptr;  
  
__declspec(restrict) float * ma(int size)  
{  
    float * retval;  
    retval = memptr;  
    memptr += size;  
    return retval;  
}  
  
__declspec(restrict) float * init(int m, int n)  
{  
    float * a;  
    int i, j;  
    int k=1;  
  
    a = ma(m * n);  
    if (!a) exit(1);  
    for (i=0; i<m; i++)  
        for (j=0; j<n; j++)  
            a[i*n+j] = 0.1/k++;  
    return a;  
}  
  
__declspec(noalias) void multiply(float * a, float * b, float * c)  
{  
    int i, j, k;  
  
    for (j=0; j<P; j++)  
        for (i=0; i<M; i++)  
            for (k=0; k<N; k++)  
                c[i * P + j] =   
                          a[i * N + k] *   
                          b[k * P + j];  
}  
  
int main()  
{  
    float * a, * b, * c;  
  
    mempool = (float *) malloc(sizeof(float) * (M*N + N*P + M*P));  
  
    if (!mempool)   
    {  
        puts("ERROR: Malloc returned null");  
        exit(1);  
    }  
  
    memptr = mempool;  
    a = init(M, N);  
    b = init(N, P);  
    c = init(M, P);  
  
    multiply(a, b, c);  
}  
```  
  
## See Also  
 [__declspec](../vs140/__declspec.md)   
 [Keywords](../vs140/Keywords--C---.md)