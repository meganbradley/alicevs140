---
title: "invalid_scheduler_policy_thread_specification::invalid_scheduler_policy_thread_specification Constructor"
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
ms.assetid: eddb6012-41fb-44f7-9ce0-83a6be898be1
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# invalid_scheduler_policy_thread_specification::invalid_scheduler_policy_thread_specification Constructor
Constructs an `invalid_scheduler_policy_value` object.  
  
## Syntax  
  
```  
explicit _CRTIMP invalid_scheduler_policy_thread_specification(  
   _In_z_ const char * _Message  
) throw();  
  
invalid_scheduler_policy_thread_specification() throw();  
```  
  
#### Parameters  
 `_Message`  
 A descriptive message of the error.  
  
## Requirements  
 **Header:** concrt.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [invalid_scheduler_policy_thread_specification Class](../vs140/invalid_scheduler_policy_thread_specification-Class.md)