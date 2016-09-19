---
title: "barrier"
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
ms.assetid: 5c73ad4f-c768-443a-8f9e-4fd8bc2253c7
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# barrier
Synchronizes all threads in a team; all threads pause at the barrier, until all threads execute the barrier.  
  
## Syntax  
  
```  
#pragma omp barrier  
```  
  
## Remarks  
 The `barrier` directive supports no OpenMP clauses.  
  
 For more information, see [2.6.3 barrier Directive](../vs140/2.6.3-barrier-Directive.md).  
  
## Example  
 For a sample of how to use `barrier`, see [master](../vs140/master.md).  
  
## See Also  
 [Directives](../vs140/OpenMP-Directives.md)