---
title: "invalid_link_target::invalid_link_target Constructor"
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
ms.assetid: 9bff75d8-7174-46f7-9be0-dbd76cbda56e
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# invalid_link_target::invalid_link_target Constructor
Constructs an `invalid_link_target` object.  
  
## Syntax  
  
```  
explicit _CRTIMP invalid_link_target(  
   _In_z_ const char * _Message  
) throw();  
  
invalid_link_target() throw();  
```  
  
#### Parameters  
 `_Message`  
 A descriptive message of the error.  
  
## Requirements  
 **Header:** concrt.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [invalid_link_target Class](../vs140/invalid_link_target-Class.md)