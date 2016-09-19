---
title: "task_group_status Enumeration"
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
ms.assetid: fce7cc14-6cb6-43b8-82ba-f98e2225db6a
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# task_group_status Enumeration
Describes the execution status of a `task_group` or `structured_task_group` object. A value of this type is returned by numerous methods that wait on tasks scheduled to a task group to complete.  
  
## Syntax  
  
```  
enum task_group_status;  
```  
  
## Members  
  
### Values  
  
|Name|Description|  
|----------|-----------------|  
|`canceled`|The `task_group` or `structured_task_group` object was canceled. One or more tasks may not have executed.|  
|`completed`|The tasks queued to the `task_group` or `structured_task_group` object completed successfully.|  
|`not_complete`|The tasks queued to the `task_group` object have not completed. Note that this value is not presently returned by the Concurrency Runtime.|  
  
## Requirements  
 **Header:** pplinterface.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [concurrency Namespace](../vs140/concurrency-Namespace.md)   
 [task_group Class](../vs140/task_group-Class.md)   
 [task_group::wait Method](../vs140/task_group--wait-Method.md)   
 [task_group::run_and_wait Method](../vs140/task_group--run_and_wait-Method.md)   
 [structured_task_group Class](../vs140/structured_task_group-Class.md)   
 [structured_task_group::wait Method](../vs140/structured_task_group--wait-Method.md)   
 [structured_task_group::run_and_wait Method](../vs140/structured_task_group--run_and_wait-Method.md)