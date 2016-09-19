---
title: "EventSource::addRemoveLock_ Data Member"
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
ms.topic: reference
ms.assetid: e2d69256-4891-4aad-ad0b-76479c0bb076
caps.latest.revision: 5
translation.priority.ht: 
  - de-de
  - ja-jp
---
# EventSource::addRemoveLock_ Data Member
Synchronizes access to the [targets_](../vs140/EventSource--targets_-Data-Member.md) array when adding, removing, or invoking event handlers.  
  
## Syntax  
  
```  
Wrappers::SRWLock addRemoveLock_;  
```  
  
## Requirements  
 **Header:** event.h  
  
 **Namespace:** Microsoft::WRL  
  
## See Also  
 [EventSource Class](../vs140/EventSource-Class.md)