---
title: "SchedulingProtocolType Enumeration"
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
ms.assetid: a4bb87b9-bec3-4918-bb06-1993c53e1069
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# SchedulingProtocolType Enumeration
Used by the `SchedulingProtocol` policy to describe which scheduling algorithm will be utilized for the scheduler. For more information on available scheduler policies, see [PolicyElementKey Enumeration](../vs140/PolicyElementKey-Enumeration.md).  
  
## Syntax  
  
```  
enum SchedulingProtocolType;  
```  
  
## Members  
  
### Values  
  
|Name|Description|  
|----------|-----------------|  
|`EnhanceForwardProgress`|The scheduler prefers to round-robin through schedule groups after executing each task. Unblocked contexts are typically scheduled in a first-in-first-out (FIFO) fashion. Virtual processors do not cache unblocked contexts.|  
|`EnhanceScheduleGroupLocality`|The scheduler prefers to continue to work on tasks within the current schedule group before moving to another schedule group. Unblocked contexts are cached per virtual-processor and are typically scheduled in a last-in-first-out (LIFO) fashion by the virtual processor which unblocked them.|  
  
## Requirements  
 **Header:** concrt.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [concurrency Namespace](../vs140/concurrency-Namespace.md)   
 [SchedulerPolicy Class](../vs140/SchedulerPolicy-Class.md)   
 [PolicyElementKey Enumeration](../vs140/PolicyElementKey-Enumeration.md)