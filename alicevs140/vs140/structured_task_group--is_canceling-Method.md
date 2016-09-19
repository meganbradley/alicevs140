---
title: "structured_task_group::is_canceling Method"
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
ms.assetid: 07e4e74d-fe7f-4899-8fbc-3d51cfd878ea
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# structured_task_group::is_canceling Method
Informs the caller whether or not the task group is currently in the midst of a cancellation. This does not necessarily indicate that the `cancel` method was called on the `structured_task_group` object (although such certainly qualifies this method to return `true`). It may be the case that the `structured_task_group` object is executing inline and a task group further up in the work tree was canceled. In cases such as these where the runtime can determine ahead of time that cancellation will flow through this `structured_task_group` object, `true` will be returned as well.  
  
## Syntax  
  
```  
bool is_canceling();  
```  
  
## Return Value  
 An indication of whether the `structured_task_group` object is in the midst of a cancellation (or is guaranteed to be shortly).  
  
## Remarks  
 For more information, see [Cancellation in the PPL](../vs140/Cancellation-in-the-PPL.md).  
  
## Requirements  
 **Header:** ppl.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [structured_task_group Class](../vs140/structured_task_group-Class.md)