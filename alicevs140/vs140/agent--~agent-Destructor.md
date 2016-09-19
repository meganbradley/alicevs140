---
title: "agent::~agent Destructor"
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
ms.assetid: b99ee6df-4d91-49a8-9f1a-2f83c9484332
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# agent::~agent Destructor
Destroys the agent.  
  
## Syntax  
  
```  
virtual ~agent();  
```  
  
## Remarks  
 It is an error to destroy an agent that is not in a terminal state (either `agent_done` or `agent_canceled`). This can be avoided by waiting for the agent to reach a terminal state in the destructor of a class that inherits from the `agent` class.  
  
## Requirements  
 **Header:** agents.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [agent Class](../vs140/agent-Class.md)