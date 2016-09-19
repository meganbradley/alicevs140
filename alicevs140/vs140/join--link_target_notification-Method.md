---
title: "join::link_target_notification Method"
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
ms.assetid: ec4af4bb-11e1-4fad-b3dd-c88098c47e01
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# join::link_target_notification Method
A callback that notifies that a new target has been linked to this `join` messaging block.  
  
## Syntax  
  
```  
virtual void link_target_notification(  
   _Inout_ ITarget<std::vector<_Type>> *  
);  
```  
  
## Requirements  
 **Header:** agents.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [join Class](../vs140/join-Class.md)