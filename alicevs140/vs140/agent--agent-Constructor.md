---
title: "agent::agent Constructor"
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
ms.assetid: d13a380a-e3fb-4932-8785-09b4cdb1f0e6
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# agent::agent Constructor
Constructs an agent.  
  
## Syntax  
  
```  
agent();  
  
agent(  
   Scheduler& _PScheduler  
);  
  
agent(  
   ScheduleGroup& _PGroup  
);  
```  
  
#### Parameters  
 `_PScheduler`  
 The `Scheduler` object within which the execution task of the agent is scheduled.  
  
 `_PGroup`  
 The `ScheduleGroup` object within which the execution task of the agent is scheduled. The `Scheduler` object used is implied by the schedule group.  
  
## Remarks  
 The runtime uses the default scheduler if you do not specify the `_PScheduler` or `_PGroup` parameters.  
  
## Requirements  
 **Header:** agents.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [agent Class](../vs140/agent-Class.md)   
 [Scheduler Class](../vs140/Scheduler-Class.md)   
 [ScheduleGroup Class](../vs140/ScheduleGroup-Class.md)