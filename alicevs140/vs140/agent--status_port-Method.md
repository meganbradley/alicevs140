---
title: "agent::status_port Method"
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
ms.assetid: 156f87b1-13f8-4a8a-9bf1-7b0b0ecc5fc8
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# agent::status_port Method
An asynchronous source of status information from the agent.  
  
## Syntax  
  
```  
ISource<agent_status> * status_port();  
```  
  
## Return Value  
 Returns a message source that can send messages about the current state of the agent.  
  
## Requirements  
 **Header:** agents.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [agent Class](../vs140/agent-Class.md)