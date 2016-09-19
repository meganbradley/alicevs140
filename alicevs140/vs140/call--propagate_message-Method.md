---
title: "call::propagate_message Method"
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
ms.assetid: 5ed1f32e-6bea-49f2-b8a1-ff254996e014
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# call::propagate_message Method
Asynchronously passes a message from an `ISource` block to this `call` messaging block. It is invoked by the `propagate` method, when called by a source block.  
  
## Syntax  
  
```  
virtual message_status propagate_message(  
   _Inout_ message<_Type> * _PMessage,  
   _Inout_ ISource<_Type> * _PSource  
);  
```  
  
#### Parameters  
 `_PMessage`  
 A pointer to the `message` object.  
  
 `_PSource`  
 A pointer to the source block offering the message.  
  
## Return Value  
 A [message_status](../vs140/message_status-Enumeration.md) indication of what the target decided to do with the message.  
  
## Requirements  
 **Header:** agents.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [call Class](../vs140/call-Class.md)