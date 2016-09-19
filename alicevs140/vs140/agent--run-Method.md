---
title: "agent::run Method"
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
ms.assetid: 21882c7a-3428-4671-ad3d-de1c83eda21f
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# agent::run Method
Represents the main task of an agent. `run` should be overridden in a derived class, and specifies what the agent should do after it has been started.  
  
## Syntax  
  
```  
virtual void run() = 0;  
```  
  
## Remarks  
 The agent status is changed to `agent_started` right before this method is invoked. The method should invoke `done` on the agent with an appropriate status before returning, and may not throw any exceptions.  
  
## Requirements  
 **Header:** agents.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [agent Class](../vs140/agent-Class.md)