---
title: "target_block::propagate_message Method"
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
ms.assetid: 606df8fd-0cdb-421e-8628-2584dc2f769f
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# target_block::propagate_message Method
When overridden in a derived class, this method asynchronously passes a message from an `ISource` block to this `target_block` object. It is invoked by the `propagate` method, when called by a source block.  
  
## Syntax  
  
```  
virtual message_status propagate_message(  
   _Inout_ message<_Source_type> * _PMessage,  
   _Inout_ ISource<_Source_type> * _PSource  
) = 0;  
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
 [target_block Class](../vs140/target_block-Class.md)