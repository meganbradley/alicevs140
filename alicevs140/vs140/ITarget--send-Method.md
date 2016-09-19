---
title: "ITarget::send Method"
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
ms.assetid: 8730c491-4780-487d-b21d-2a7348972b41
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ITarget::send Method
When overridden in a derived class, synchronously passes a message to the target block.  
  
## Syntax  
  
```  
virtual message_status send(  
   _Inout_ message<_Type> * _PMessage,  
   _Inout_ ISource<_Type> * _PSource  
) = 0;  
```  
  
#### Parameters  
 `_PMessage`  
 A pointer to the `message` object.  
  
 `_PSource`  
 A pointer to the source block offering the message.  
  
## Return Value  
 A [message_status](../vs140/message_status-Enumeration.md) indication of what the target decided to do with the message.  
  
## Remarks  
 The method throws an [invalid_argument](../vs140/invalid_argument-Class.md) exception if either the `_PMessage` or `_PSource` parameter is `NULL`.  
  
 Using the `send` method outside of message initiation and to propagate messages within a network is dangerous and can lead to deadlock.  
  
 When `send` returns, the message has either already been accepted, and transferred into the target block, or it has been declined by the target.  
  
## Requirements  
 **Header:** agents.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [ITarget Class](../vs140/ITarget-Class.md)