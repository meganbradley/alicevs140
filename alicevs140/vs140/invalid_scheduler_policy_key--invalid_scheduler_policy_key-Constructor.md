---
title: "invalid_scheduler_policy_key::invalid_scheduler_policy_key Constructor"
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
ms.assetid: cd75aa9b-7c04-472e-85d5-fdb7ef37d6d6
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# invalid_scheduler_policy_key::invalid_scheduler_policy_key Constructor
Constructs an `invalid_scheduler_policy_key` object.  
  
## Syntax  
  
```  
explicit _CRTIMP invalid_scheduler_policy_key(  
   _In_z_ const char * _Message  
) throw();  
  
invalid_scheduler_policy_key() throw();  
```  
  
#### Parameters  
 `_Message`  
 A descriptive message of the error.  
  
## Requirements  
 **Header:** concrt.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [invalid_scheduler_policy_key Class](../vs140/invalid_scheduler_policy_key-Class.md)