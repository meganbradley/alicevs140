---
title: "source_block::consume_message Method"
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
ms.assetid: 1d20e951-ef02-40c3-aa61-048723623ca9
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# source_block::consume_message Method
When overridden in a derived class, consumes a message that was previously reserved.  
  
## Syntax  
  
```  
virtual message<_Target_type> * consume_message(  
   runtime_object_identity _MsgId  
) = 0;  
```  
  
#### Parameters  
 `_MsgId`  
 The `runtime_object_identity` of the `message` object being consumed.  
  
## Return Value  
 A pointer to the message that the caller now has ownership of.  
  
## Remarks  
 Similar to `accept`, but is always preceded by a call to `reserve`.  
  
## Requirements  
 **Header:** agents.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [source_block Class](../vs140/source_block-Class.md)