---
title: "message_processor::wait Method"
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
ms.assetid: 9ce7edca-f5b0-4af5-9f73-20265e56639c
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# message_processor::wait Method
When overridden in a derived class, waits for all asynchronous operations to complete.  
  
## Syntax  
  
```  
virtual void wait() = 0;  
```  
  
## Remarks  
 Processor implementations should override this method.  
  
## Requirements  
 **Header:** agents.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [message_processor Class](../vs140/message_processor-Class.md)