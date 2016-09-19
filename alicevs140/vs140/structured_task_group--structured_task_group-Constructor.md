---
title: "structured_task_group::structured_task_group Constructor"
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
ms.assetid: ff9b0b46-42a8-4fe6-8353-59cdf3c921b3
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# structured_task_group::structured_task_group Constructor
Constructs a new `structured_task_group` object.  
  
## Syntax  
  
```  
structured_task_group();  
  
structured_task_group(  
   cancellation_token _CancellationToken  
);  
```  
  
#### Parameters  
 `_CancellationToken`  
 A cancellation token to associate with this structured task group. The structured task group will be canceled when the token is canceled.  
  
## Remarks  
 The constructor that takes a cancellation token creates a `structured_task_group` that will be canceled when the source associated with the token is canceled. Providing an explicit cancellation token also isolates this structured task group from participating in an implicit cancellation from a parent group with a different token or no token.  
  
## Requirements  
 **Header:** ppl.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [structured_task_group Class](../vs140/structured_task_group-Class.md)   
 [Task Parallelism](../vs140/Task-Parallelism--Concurrency-Runtime-.md)