---
title: "source_block::accept_message Method"
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
ms.assetid: 7c1f52be-d7be-42ff-bf33-d59bb2466f13
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# source_block::accept_message Method
When overridden in a derived class, accepts an offered message by the source. Message blocks should override this method to validate the `_MsgId` and return a message.  
  
## Syntax  
  
```  
virtual message<_Target_type> * accept_message(  
   runtime_object_identity _MsgId  
) = 0;  
```  
  
#### Parameters  
 `_MsgId`  
 The runtime object identity of the `message` object.  
  
## Return Value  
 A pointer to the message that the caller now has ownership of.  
  
## Remarks  
 To transfer ownership, the original message pointer should be returned. To maintain ownership, a copy of message payload needs to be made and returned.  
  
## Requirements  
 **Header:** agents.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [source_block Class](../vs140/source_block-Class.md)