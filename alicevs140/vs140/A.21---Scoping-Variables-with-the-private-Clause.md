---
title: "A.21   Scoping Variables with the private Clause"
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
ms.assetid: 7cdb4a7f-af24-44ac-9d33-e43840bc8f3d
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# A.21   Scoping Variables with the private Clause
The values of `i` and `j` in the following example are undefined on exit from the parallel region:  
  
```  
int i, j;  
i = 1;  
j = 2;  
#pragma omp parallel private(i) firstprivate(j)  
{  
  i = 3;  
  j = j + 2;  
}  
printf_s("%d %d\n", i, j);  
```  
  
 For more information on the `private` clause, see [Section 2.7.2.1](../vs140/2.7.2.1-private.md) on page 25.