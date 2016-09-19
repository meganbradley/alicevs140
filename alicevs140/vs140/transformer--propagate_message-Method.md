---
title: "transformer::propagate_message Method"
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
ms.assetid: ab7669a0-0e90-4911-a1fb-9ca6c3973b83
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# transformer::propagate_message Method
Asynchronously passes a message from an `ISource` block to this `transformer` messaging block. It is invoked by the `propagate` method, when called by a source block.  
  
## Syntax  
  
```  
virtual message_status propagate_message(  
   _Inout_ message<_Input> * _PMessage,  
   _Inout_ ISource<_Input> * _PSource  
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
 [transformer Class](../vs140/transformer-Class.md)