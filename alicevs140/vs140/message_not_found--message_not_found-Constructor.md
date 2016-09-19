---
title: "message_not_found::message_not_found Constructor"
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
ms.assetid: 0b064ccd-60d4-40e1-909d-c0f3fa2cc0b1
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# message_not_found::message_not_found Constructor
Constructs a `message_not_found` object.  
  
## Syntax  
  
```  
explicit _CRTIMP message_not_found(  
   _In_z_ const char * _Message  
) throw();  
  
message_not_found() throw();  
```  
  
#### Parameters  
 `_Message`  
 A descriptive message of the error.  
  
## Requirements  
 **Header:** concrt.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [message_not_found Class](../vs140/message_not_found-Class.md)