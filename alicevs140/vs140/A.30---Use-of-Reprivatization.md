---
title: "A.30   Use of Reprivatization"
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
ms.assetid: 26529090-6c39-40f2-b806-e12374d6b5f8
caps.latest.revision: 7
translation.priority.ht: 
  - de-de
  - ja-jp
---
# A.30   Use of Reprivatization
The following example demonstrates the reprivatization of variables. Private variables can be marked `private` again in a nested directive. They do not have to be shared in the enclosing parallel region.  
  
```  
int i, a;  
...  
#pragma omp parallel private(a)  
{  
  ...  
  #pragma omp parallel for private(a)  
  for (i=0; i<10; i++)  
     {  
       ...  
     }  
}  
```