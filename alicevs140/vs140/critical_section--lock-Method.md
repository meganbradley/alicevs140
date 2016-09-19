---
title: "critical_section::lock Method"
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
ms.assetid: 62cc3d7b-4331-403e-8595-d07ff24023e4
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# critical_section::lock Method
Acquires this critical section.  
  
## Syntax  
  
```  
void lock();  
```  
  
## Remarks  
 It is often safer to utilize the [scoped_lock](../vs140/critical_section--scoped_lock-Class.md) construct to acquire and release a `critical_section` object in an exception safe way.  
  
 If the lock is already held by the calling context, an [improper_lock](../vs140/improper_lock-Class.md) exception will be thrown.  
  
## Requirements  
 **Header:** concrt.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [critical_section Class](../vs140/critical_section-Class.md)   
 [critical_section::unlock Method](../vs140/critical_section--unlock-Method.md)   
 [critical_section::scoped_lock Class](../vs140/critical_section--scoped_lock-Class.md)