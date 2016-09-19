---
title: "Lightweight Tasks"
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
ms.assetid: b6dcfc7a-9fa9-4144-96a6-2845ea272017
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Lightweight Tasks
This document describes the role of lightweight tasks in the Concurrency Runtime. A *lightweight task* is a task that you schedule directly from a `concurrency::Scheduler` or `concurrency::ScheduleGroup` object. A lightweight task resembles the function that you provide to the Windows API [CreateThread](http://msdn.microsoft.com/library/windows/desktop/ms682453) function. Therefore, lightweight tasks are useful when you adapt existing code to use the scheduling functionality of the Concurrency Runtime. The Concurrency Runtime itself uses lightweight tasks to schedule asynchronous agents and send messages between asynchronous message blocks.  
  
> [!TIP]
>  The Concurrency Runtime provides a default scheduler, and therefore you are not required to create one in your application. Because the Task Scheduler helps you fine-tune the performance of your applications, we recommend that you start with the [Parallel Patterns Library (PPL)](../vs140/Parallel-Patterns-Library--PPL-.md) or the [Asynchronous Agents Library](../vs140/Asynchronous-Agents-Library.md) if you are new to the Concurrency Runtime.  
  
 Lightweight tasks carry less overhead than asynchronous agents and task groups. For example, the runtime does not inform you when a lightweight task finishes. In addition, the runtime does not catch or handle exceptions that are thrown from a lightweight task. For more information about exception handling and lightweight tasks, see [Exception Handling in the Concurrency Runtime](../vs140/Exception-Handling-in-the-Concurrency-Runtime.md).  
  
 For most tasks, we recommend that you use more robust functionality such as task groups and parallel algorithms because they let you more easily break complex tasks into more basic ones. For more information about task groups, see [Task Parallelism](../vs140/Task-Parallelism--Concurrency-Runtime-.md). For more information about parallel algorithms, see [Parallel Algorithms](../vs140/Parallel-Algorithms.md).  
  
 To create a lightweight task, call the [concurrency::ScheduleGroup::ScheduleTask](../vs140/ScheduleGroup--ScheduleTask-Method.md), [concurrency::CurrentScheduler::ScheduleTask](../vs140/CurrentScheduler--ScheduleTask-Method.md), or [concurrency::Scheduler::ScheduleTask](../vs140/Scheduler--ScheduleTask-Method.md) method. To wait for a lightweight task to finish, wait for the parent scheduler to shut down or use a synchronization mechanism such as a [concurrency::event](../vs140/event-Class.md) object.  
  
## Example  
 For an example that demonstrates how to adapt existing code to use a lightweight task, see [Walkthough: Adapting Existing Code to Use Lightweight Tasks](../vs140/Walkthrough--Adapting-Existing-Code-to-Use-Lightweight-Tasks.md).  
  
## See Also  
 [Task Scheduler (Concurrency Runtime)](../vs140/Task-Scheduler--Concurrency-Runtime-.md)   
 [Walkthough: Adapting Existing Code to Use Lightweight Tasks](../vs140/Walkthrough--Adapting-Existing-Code-to-Use-Lightweight-Tasks.md)