---
title: "propagator_block::send_message Method"
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
ms.assetid: ac572d55-13ee-46a3-95ed-8880995d749d
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# propagator_block::send_message Method
When overridden in a derived class, this method synchronously passes a message from an `ISource` block to this `propagator_block` object. It is invoked by the `send` method, when called by a source block.  
  
## Syntax  
  
```  
virtual message_status send_message(  
   _Inout_ message<_Source_type> *,  
   _Inout_ ISource<_Source_type> *  
);  
```  
  
## Return Value  
 A [message_status](../vs140/message_status-Enumeration.md) indication of what the target decided to do with the message.  
  
## Remarks  
 By default, this block returns `declined` unless overridden by a derived class.  
  
## Requirements  
 **Header:** agents.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [propagator_block Class](../vs140/propagator_block-Class.md)