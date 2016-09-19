---
title: "structured_task_group::run_and_wait Method"
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
ms.assetid: 37677993-f3b2-4d89-99e8-1869b1ca74e1
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# structured_task_group::run_and_wait Method
Schedules a task to be run inline on the calling context with the assistance of the `structured_task_group` object for full cancellation support. If a `task_handle` object is passed as a parameter to `run_and_wait`, the caller is responsible for managing the lifetime of the `task_handle` object. The function then waits until all work on the `structured_task_group` object has either completed or been canceled.  
  
## Syntax  
  
```  
template<  
   class _Function  
>  
task_group_status run_and_wait(  
   task_handle<_Function>& _Task_handle  
);  
  
template<  
   class _Function  
>  
task_group_status run_and_wait(  
   const _Function& _Func  
);  
```  
  
#### Parameters  
 `_Function`  
 The type of the function object that will be invoked to execute the task.  
  
 `_Task_handle`  
 A handle to the task which will be run inline on the calling context. Note that the caller has responsibility for the lifetime of this object. The runtime will continue to expect it to live until the `run_and_wait` method finishes execution.  
  
 `_Func`  
 A function which will be called to invoke the body of the work. This may be a lambda or other object which supports a version of the function call operator with the signature `void operator()()`.  
  
## Return Value  
 An indication of whether the wait was satisfied or the task group was canceled, due to either an explicit cancel operation or an exception being thrown from one of its tasks. For more information, see [task_group_status](../vs140/task_group_status-Enumeration.md)  
  
## Remarks  
 Note that one or more of the tasks scheduled to this `structured_task_group` object may execute inline on the calling context.  
  
 If one or more of the tasks scheduled to this `structured_task_group` object throws an exception, the runtime will select one such exception of its choosing and propagate it out of the call to the `run_and_wait` method.  
  
 After this function returns, the `structured_task_group` object is considered in a final state and should not be used. Note that utilization after the `run_and_wait` method returns will result in undefined behavior.  
  
 In the non-exceptional path of execution, you have a mandate to call either this method or the `wait` method before the destructor of the `structured_task_group` executes.  
  
## Requirements  
 **Header:** ppl.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [structured_task_group Class](../vs140/structured_task_group-Class.md)   
 [structured_task_group::run Method](../vs140/structured_task_group--run-Method.md)   
 [structured_task_group::wait Method](../vs140/structured_task_group--wait-Method.md)   
 [Task Parallelism](../vs140/Task-Parallelism--Concurrency-Runtime-.md)