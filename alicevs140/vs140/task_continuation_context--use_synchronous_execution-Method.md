---
title: "task_continuation_context::use_synchronous_execution Method"
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
ms.assetid: 88a0a1e0-fb27-4e2c-87a1-1f3e44ecf839
caps.latest.revision: 7
---
# task_continuation_context::use_synchronous_execution Method
Returns a task continuation context object that represents the synchronous execution context.  
  
## Syntax  
  
```  
static task_continuation_context use_synchronous_execution();  
```  
  
## Return Value  
 The synchronous execution context.  
  
## Remarks  
 The `use_synchronous_execution` method forces the continuation task to run synchronously on the context, causing its antecedent task's completion.  
  
 If the antecedent task has already completed when the continuation is attached, the continuation runs synchronously on the context that attaches the continuation.  
  
## Requirements  
 **Header:** ppltasks.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [task_continuation_context Class](../vs140/task_continuation_context-Class.md)