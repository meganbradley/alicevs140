---
title: "task::get Method"
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
ms.assetid: 487483a1-a9a1-4fe1-83ae-c3c19ce54bd0
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# task::get Method
Returns the result this task produced. If the task is not in a terminal state, a call to `get` will wait for the task to finish. This method does not return a value when called on a task with a `result_type` of `void`.  
  
## Syntax  
  
```  
_ReturnType get() const;  
  
void get() const;  
```  
  
## Return Value  
 The result of the task.  
  
## Remarks  
 If the task is canceled, a call to `get` will throw a [task_canceled](../vs140/task_canceled-Class.md) exception. If the task encountered an different exception or an exception was propagated to it from an antecedent task, a call to `get` will throw that exception.  
  
> [!IMPORTANT]
>  In a [!INCLUDE[win8_appname_long](../vs140/includes/win8_appname_long_md.md)] app, do not call [concurrency::task::wait](../vs140/task--wait-Method.md) or `get` (`wait` calls `get`) in code that runs on the STA. Otherwise, the runtime throws [concurrency::invalid_operation](../vs140/invalid_operation-Class.md) because these methods block the current thread and can cause the app to become unresponsive. However, you can call the `get` method to receive the result of the antecedent task in a task-based continuation because the result is immediately available.  
  
## Requirements  
 **Header:** ppltasks.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [task Class (Concurrency Runtime)](../vs140/task-Class--Concurrency-Runtime-.md)