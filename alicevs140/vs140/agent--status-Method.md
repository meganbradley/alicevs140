---
title: "agent::status Method"
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
ms.assetid: 057aab3c-8fbb-4425-b45c-cb8cf4297c64
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# agent::status Method
A synchronous source of status information from the agent.  
  
## Syntax  
  
```  
agent_status status();  
```  
  
## Return Value  
 Returns the current state of the agent. Note that this returned state could change immediately after being returned.  
  
## Requirements  
 **Header:** agents.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [agent Class](../vs140/agent-Class.md)   
 [agent_status Enumeration](../vs140/agent_status-Enumeration.md)