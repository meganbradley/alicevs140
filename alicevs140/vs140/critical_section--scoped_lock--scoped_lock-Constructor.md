---
title: "critical_section::scoped_lock::scoped_lock Constructor"
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
ms.assetid: 8ce55ee9-e72d-4475-b3f1-84aea7d6dd3a
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# critical_section::scoped_lock::scoped_lock Constructor
Constructs a `scoped_lock` object and acquires the `critical_section` object passed in the `_Critical_section` parameter. If the critical section is held by another thread, this call will block.  
  
## Syntax  
  
```  
explicit _CRTIMP scoped_lock(  
   critical_section& _Critical_section  
);  
```  
  
#### Parameters  
 `_Critical_section`  
 The critical section to lock.  
  
## Requirements  
 **Header:** concrt.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [critical_section::scoped_lock Class](../vs140/critical_section--scoped_lock-Class.md)   
 [critical_section Class](../vs140/critical_section-Class.md)