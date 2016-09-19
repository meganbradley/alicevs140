---
title: "Scheduler::GetPolicy Method"
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
ms.assetid: db8ccac3-7b62-4321-a056-5861d2ac719b
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Scheduler::GetPolicy Method
Returns a copy of the policy that the scheduler was created with.  
  
## Syntax  
  
```  
virtual SchedulerPolicy GetPolicy() const =0;  
```  
  
## Return Value  
 A copy of the policy that the scheduler was created with.  
  
## Requirements  
 **Header:** concrt.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [Scheduler Class](../vs140/Scheduler-Class.md)   
 [SchedulerPolicy Class](../vs140/SchedulerPolicy-Class.md)   
 [PolicyElementKey Enumeration](../vs140/PolicyElementKey-Enumeration.md)   
 [Task Scheduler (Concurrency Runtime)](../vs140/Task-Scheduler--Concurrency-Runtime-.md)