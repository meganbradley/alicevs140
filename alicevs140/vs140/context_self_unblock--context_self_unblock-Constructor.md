---
title: "context_self_unblock::context_self_unblock Constructor"
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
ms.assetid: 6d62972c-e329-4eca-8a23-f68d6842cc84
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# context_self_unblock::context_self_unblock Constructor
Constructs a `context_self_unblock` object.  
  
## Syntax  
  
```  
explicit _CRTIMP context_self_unblock(  
   _In_z_ const char * _Message  
) throw();  
  
context_self_unblock() throw();  
```  
  
#### Parameters  
 `_Message`  
 A descriptive message of the error.  
  
## Requirements  
 **Header:** concrt.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [context_self_unblock Class](../vs140/context_self_unblock-Class.md)