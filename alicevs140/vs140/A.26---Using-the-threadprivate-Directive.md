---
title: "A.26   Using the threadprivate Directive"
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
ms.assetid: 6eda76c2-c4f1-4208-a900-e0ea98a53eca
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# A.26   Using the threadprivate Directive
The following examples demonstrate how to use the `threadprivate` directive  ([Section 2.7.1](../vs140/2.7.1-threadprivate-Directive.md) on page 23) to give each thread a separate counter.  
  
 **Example 1:**  
  
```  
int counter = 0;  
#pragma omp threadprivate(counter)  
  
int sub()  
{  
    counter++;  
    return(counter);  
}  
```  
  
 **Example 2:**  
  
```  
int sub()  
{  
    static int counter = 0;  
    #pragma omp threadprivate(counter)  
    counter++;  
    return(counter);  
}  
```