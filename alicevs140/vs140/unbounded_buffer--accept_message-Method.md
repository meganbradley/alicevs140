---
title: "unbounded_buffer::accept_message Method"
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
ms.assetid: d7fa32b2-c61f-4286-b4ec-9666dbb3e0fb
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# unbounded_buffer::accept_message Method
Accepts a message that was offered by this `unbounded_buffer` messaging block, transferring ownership to the caller.  
  
## Syntax  
  
```  
virtual message<_Type> * accept_message(  
   runtime_object_identity _MsgId  
);  
```  
  
#### Parameters  
 `_MsgId`  
 The `runtime_object_identity` of the offered `message` object.  
  
## Return Value  
 A pointer to the `message` object that the caller now has ownership of.  
  
## Requirements  
 **Header:** agents.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [unbounded_buffer Class](../vs140/unbounded_buffer-Class.md)