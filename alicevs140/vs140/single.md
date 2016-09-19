---
title: "single"
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
ms.assetid: 85cf94fb-cb9c-4d82-8609-adffa9f552e1
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# single
Lets you specify that a section of code should be executed on a single thread, not necessarily the master thread.  
  
## Syntax  
  
```  
#pragma omp single [clauses]   
{  
   code_block   
}  
```  
  
#### Parameters  
 `clause` (optional)  
 Zero or more clauses. See the Remarks section for a list of the clauses supported by **single**.  
  
## Remarks  
 The **single** directive supports the following OpenMP clauses:  
  
-   [copyprivate](../vs140/copyprivate.md)  
  
-   [firstprivate](../vs140/firstprivate.md)  
  
-   [nowait](../vs140/nowait.md)  
  
-   [private](../vs140/private--OpenMP-.md)  
  
 The [master](../vs140/master.md) directive lets you specify that a section of code should be executed only on the master thread.  
  
 For more information, see [2.4.3 single Construct](../vs140/2.4.3-single-Construct.md).  
  
## Example  
  
```  
// omp_single.cpp  
// compile with: /openmp   
#include <stdio.h>  
#include <omp.h>  
  
int main() {  
   #pragma omp parallel num_threads(2)  
   {  
      #pragma omp single  
      // Only a single thread can read the input.  
      printf_s("read input\n");  
  
      // Multiple threads in the team compute the results.  
      printf_s("compute results\n");  
  
      #pragma omp single  
      // Only a single thread can write the output.  
      printf_s("write output\n");  
    }  
}  
```  
  
 **read input**  
**compute results**  
**compute results**  
**write output**   
## See Also  
 [Directives](../vs140/OpenMP-Directives.md)