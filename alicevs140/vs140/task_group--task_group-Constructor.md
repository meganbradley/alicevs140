---
title: "task_group::task_group Constructor"
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
ms.assetid: cb077e36-6547-46aa-a991-5e05bb4fa511
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# task_group::task_group Constructor
Constructs a new `task_group` object.  
  
## Syntax  
  
```  
task_group();  
  
task_group(  
   cancellation_token _CancellationToken  
);  
```  
  
#### Parameters  
 `_CancellationToken`  
 A cancellation token to associate with this task group. The task group will be canceled when the token is canceled.  
  
## Remarks  
 The constructor that takes a cancellation token creates a `task_group` that will be canceled when the source associated with the token is canceled. Providing an explicit cancellation token also isolates this task group from participating in an implicit cancellation from a parent group with a different token or no token.  
  
## Requirements  
 **Header:** ppl.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [task_group Class](../vs140/task_group-Class.md)   
 [Task Parallelism](../vs140/Task-Parallelism--Concurrency-Runtime-.md)