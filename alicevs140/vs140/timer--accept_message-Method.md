---
title: "timer::accept_message Method"
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
ms.assetid: 075ffc3c-ce5c-4859-b2f2-717b3eefa5ac
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# timer::accept_message Method
Accepts a message that was offered by this `timer` messaging block, transferring ownership to the caller.  
  
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
 [timer Class](../vs140/timer-Class.md)