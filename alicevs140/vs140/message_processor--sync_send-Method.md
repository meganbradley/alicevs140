---
title: "message_processor::sync_send Method"
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
ms.assetid: 724e7fcf-10d8-47db-8dd2-beb56b6fd1fe
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# message_processor::sync_send Method
When overridden in a derived class, places messages into the block synchronously.  
  
## Syntax  
  
```  
virtual void sync_send(  
   _Inout_opt_ message<_Type> * _Msg  
) = 0;  
```  
  
#### Parameters  
 `_Msg`  
 A `message` object to send synchronously.  
  
## Remarks  
 Processor implementations should override this method.  
  
## Requirements  
 **Header:** agents.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [message_processor Class](../vs140/message_processor-Class.md)