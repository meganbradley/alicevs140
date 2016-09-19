---
title: "source_block::async_send Method"
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
ms.assetid: c2f139ae-6443-4a85-852a-d96db3e7bf93
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# source_block::async_send Method
Asynchronously queues up messages and starts a propagation task, if this has not been done already  
  
## Syntax  
  
```  
virtual void async_send(  
   _Inout_opt_ message<_Target_type> * _Msg  
);  
```  
  
#### Parameters  
 `_Msg`  
 A pointer to a `message` object to asynchronously send.  
  
## Requirements  
 **Header:** agents.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [source_block Class](../vs140/source_block-Class.md)