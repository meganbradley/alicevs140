---
title: "default_scheduler_exists::default_scheduler_exists Constructor"
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
ms.assetid: 4b19ea9d-da0d-45d7-8720-7023876f189d
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# default_scheduler_exists::default_scheduler_exists Constructor
Constructs a `default_scheduler_exists` object.  
  
## Syntax  
  
```  
explicit _CRTIMP default_scheduler_exists(  
   _In_z_ const char * _Message  
) throw();  
  
default_scheduler_exists() throw();  
```  
  
#### Parameters  
 `_Message`  
 A descriptive message of the error.  
  
## Requirements  
 **Header:** concrt.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [default_scheduler_exists Class](../vs140/default_scheduler_exists-Class.md)