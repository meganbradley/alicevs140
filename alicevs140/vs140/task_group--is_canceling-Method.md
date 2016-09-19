---
title: "task_group::is_canceling Method"
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
ms.assetid: f3c4e5cf-f109-47ea-99b5-9fba937933a1
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# task_group::is_canceling Method
Informs the caller whether or not the task group is currently in the midst of a cancellation. This does not necessarily indicate that the `cancel` method was called on the `task_group` object (although such certainly qualifies this method to return `true`). It may be the case that the `task_group` object is executing inline and a task group further up in the work tree was canceled. In cases such as these where the runtime can determine ahead of time that cancellation will flow through this `task_group` object, `true` will be returned as well.  
  
## Syntax  
  
```  
bool is_canceling();  
```  
  
## Return Value  
 An indication of whether the `task_group` object is in the midst of a cancellation (or is guaranteed to be shortly).  
  
## Remarks  
 For more information, see [Cancellation in the PPL](../vs140/Cancellation-in-the-PPL.md).  
  
## Requirements  
 **Header:** ppl.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [task_group Class](../vs140/task_group-Class.md)