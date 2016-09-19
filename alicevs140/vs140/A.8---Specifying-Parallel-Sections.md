---
title: "A.8   Specifying Parallel Sections"
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
ms.assetid: cf399304-121e-4c07-9829-47e0dbc2ef10
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# A.8   Specifying Parallel Sections
In the following example, (for [Section 2.4.2](../vs140/2.4.2-sections-Construct.md) on page 14) functions *xaxis*, *yaxis*, and *zaxis* can be executed concurrently. The first `section` directive is optional.  Note that all `section` directives need to appear in the lexical extent of the `parallel``sections` construct.  
  
```  
#pragma omp parallel sections  
{  
    #pragma omp section  
        xaxis();  
    #pragma omp section  
        yaxis();  
    #pragma omp section  
        zaxis();  
}  
```