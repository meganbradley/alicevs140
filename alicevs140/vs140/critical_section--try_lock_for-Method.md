---
title: "critical_section::try_lock_for Method"
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
ms.assetid: 831d7fe2-d560-467c-b784-20874f5dc02b
caps.latest.revision: 7
translation.priority.ht: 
  - de-de
  - ja-jp
---
# critical_section::try_lock_for Method
Tries to acquire the lock without blocking for a specific number of milliseconds.  
  
## Syntax  
  
```  
bool try_lock_for(  
   unsigned int _Timeout  
);  
```  
  
#### Parameters  
 `_Timeout`  
 The number of milliseconds to wait before timing out.  
  
## Return Value  
 If the lock was acquired, the value `true`; otherwise, the value `false`.  
  
## Requirements  
 **Header:** concrt.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [critical_section Class](../vs140/critical_section-Class.md)   
 [critical_section::unlock Method](../vs140/critical_section--unlock-Method.md)