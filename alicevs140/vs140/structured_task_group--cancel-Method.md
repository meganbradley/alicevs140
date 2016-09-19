---
title: "structured_task_group::cancel Method"
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
ms.assetid: 8b6015cd-cc68-4fe8-9467-a34386adbd69
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# structured_task_group::cancel Method
Makes a best effort attempt to cancel the sub-tree of work rooted at this task group. Every task scheduled on the task group will get canceled transitively if possible.  
  
## Syntax  
  
```  
void cancel();  
```  
  
## Remarks  
 For more information, see [Cancellation in the PPL](../vs140/Cancellation-in-the-PPL.md).  
  
## Requirements  
 **Header:** ppl.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [structured_task_group Class](../vs140/structured_task_group-Class.md)