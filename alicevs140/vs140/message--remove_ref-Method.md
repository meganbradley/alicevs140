---
title: "message::remove_ref Method"
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
ms.assetid: f6cd8a10-ee2c-4540-be0a-8bbee2ad2bfc
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# message::remove_ref Method
Subtracts from the reference count for the `message` object. Used for message blocks that need reference counting to determine message lifetimes.  
  
## Syntax  
  
```  
long remove_ref();  
```  
  
## Return Value  
 The new value of the reference count.  
  
## Requirements  
 **Header:** agents.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [message Class](../vs140/message-Class.md)