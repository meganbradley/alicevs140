---
title: "is_current_task_group_canceling Function"
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
ms.assetid: 96e07637-1683-431f-b0ac-1b85af96c9d9
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# is_current_task_group_canceling Function
Returns an indication of whether the task group which is currently executing inline on the current context is in the midst of an active cancellation (or will be shortly). Note that if there is no task group currently executing inline on the current context, `false` will be returned.  
  
## Syntax  
  
```  
bool __cdecl is_current_task_group_canceling();  
```  
  
## Return Value  
 `true` if the task group which is currently executing is canceling, `false` otherwise.  
  
## Remarks  
 For more information, see [Cancellation in the PPL](../vs140/Cancellation-in-the-PPL.md).  
  
## Requirements  
 **Header:** ppl.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [concurrency Namespace](../vs140/concurrency-Namespace.md)   
 [task_group Class](../vs140/task_group-Class.md)   
 [structured_task_group Class](../vs140/structured_task_group-Class.md)