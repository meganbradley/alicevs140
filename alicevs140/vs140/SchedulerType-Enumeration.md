---
title: "SchedulerType Enumeration"
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
ms.assetid: df44b4bc-788a-407f-a0c4-148d6876ebb2
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# SchedulerType Enumeration
Used by the `SchedulerKind` policy to describe the type of threads that the scheduler should utilize for underlying execution contexts. For more information on available scheduler policies, see [PolicyElementKey Enumeration](../vs140/PolicyElementKey-Enumeration.md).  
  
## Syntax  
  
```  
enum SchedulerType;  
```  
  
## Members  
  
### Values  
  
|Name|Description|  
|----------|-----------------|  
|`ThreadScheduler`|Indicates an explicit request of regular Win32 threads.|  
|`UmsThreadDefault`|User-mode schedulable (UMS) threads are not supported in the Concurrency Runtime in [!INCLUDE[vs_dev12](../vs140/includes/vs_dev12_md.md)]. Using `UmsThreadDefault` as a value for the `SchedulerType` policy will not result in an error. However, a scheduler created with that policy will default to using Win32 threads.|  
  
## Requirements  
 **Header:** concrt.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [concurrency Namespace](../vs140/concurrency-Namespace.md)   
 [SchedulerPolicy Class](../vs140/SchedulerPolicy-Class.md)   
 [PolicyElementKey Enumeration](../vs140/PolicyElementKey-Enumeration.md)