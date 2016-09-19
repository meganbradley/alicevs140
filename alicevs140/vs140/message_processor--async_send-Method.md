---
title: "message_processor::async_send Method"
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
ms.assetid: 74f2da2a-797b-4c3b-86f6-41807d74495a
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# message_processor::async_send Method
When overridden in a derived class, places messages into the block asynchronously.  
  
## Syntax  
  
```  
virtual void async_send(  
   _Inout_opt_ message<_Type> * _Msg  
) = 0;  
```  
  
#### Parameters  
 `_Msg`  
 A `message` object to send asynchronously.  
  
## Remarks  
 Processor implementations should override this method.  
  
## Requirements  
 **Header:** agents.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [message_processor Class](../vs140/message_processor-Class.md)