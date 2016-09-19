---
title: "critical_section::try_lock Method"
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
ms.assetid: a63f3229-2bad-4250-a35d-4c0a38b1e78a
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# critical_section::try_lock Method
Tries to acquire the lock without blocking.  
  
## Syntax  
  
```  
bool try_lock();  
```  
  
## Return Value  
 If the lock was acquired, the value `true`; otherwise, the value `false`.  
  
## Requirements  
 **Header:** concrt.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [critical_section Class](../vs140/critical_section-Class.md)   
 [critical_section::unlock Method](../vs140/critical_section--unlock-Method.md)