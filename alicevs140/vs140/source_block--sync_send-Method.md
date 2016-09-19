---
title: "source_block::sync_send Method"
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
ms.assetid: bd00839a-4b4a-4201-b5a0-3fefe89abf20
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# source_block::sync_send Method
Synchronously queues up messages and starts a propagation task, if this has not been done already.  
  
## Syntax  
  
```  
virtual void sync_send(  
   _Inout_opt_ message<_Target_type> * _Msg  
);  
```  
  
#### Parameters  
 `_Msg`  
 A pointer to a `message` object to synchronously send.  
  
## Requirements  
 **Header:** agents.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [source_block Class](../vs140/source_block-Class.md)