---
title: "ordered_message_processor::sync_send Method"
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
ms.assetid: e4634f16-3165-43d9-8ebc-546ac1b0065f
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ordered_message_processor::sync_send Method
Synchronously queues up messages and starts a processing task, if this has not been done already.  
  
## Syntax  
  
```  
virtual void sync_send(  
   _Inout_opt_ message<_Type> * _Msg  
);  
```  
  
#### Parameters  
 `_Msg`  
 A pointer to a message.  
  
## Requirements  
 **Header:** agents.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [ordered_message_processor Class](../vs140/ordered_message_processor-Class.md)