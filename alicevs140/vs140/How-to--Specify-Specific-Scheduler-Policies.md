---
title: "How to: Specify Specific Scheduler Policies"
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
ms.assetid: 9c5149f9-ac34-4ff3-9e79-0bad103e4e6b
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Specify Specific Scheduler Policies
Scheduler policies let you control the strategy that the scheduler uses when it manages tasks. This topic shows how to use a scheduler policy to increase the thread priority of a task that prints a progress indicator to the console.  
  
 For an example that uses custom scheduler policies together with asynchronous agents, see [How-to: Create Agents that Use Specific Scheduler Policies](../vs140/How-to--Create-Agents-that-Use-Specific-Scheduler-Policies.md).  
  
## Example  
 The following example performs two tasks in parallel. The first task computes the n<sup>th</sup> Fibonacci number. The second task prints a progress indicator to the console.  
  
 The first task uses recursive decomposition to compute the Fibonacci number. That is, each task recursively creates subtasks to compute the overall result. A task that uses recursive decomposition might use all available resources, and thereby starve other tasks. In this example, the task that prints the progress indicator might not receive timely access to computing resources.  
  
 To provide the task that prints a progress message fair access to computing resources, this example uses steps that are described in [How-to: Manage a Scheduler Instance](../vs140/How-to--Manage-a-Scheduler-Instance.md) to create a scheduler instance that has a custom policy. The custom policy specifies the thread priority to be the highest priority class.  
  
 This example uses the [concurrency::call](../vs140/call-Class.md) and [concurrency::timer](../vs140/timer-Class.md) classes to print the progress indicator. These classes have versions of their constructors that take a reference to a [concurrency::Scheduler](../vs140/Scheduler-Class.md) object that schedules them. The example uses the default scheduler to schedule the task that computes the Fibonacci number and the scheduler instance to schedule the task that prints the progress indicator.  
  
 To illustrate the benefits of using a scheduler that has a custom policy, this example performs the overall task two times. The example first uses the default scheduler to schedule both tasks. The example then uses the default scheduler to schedule the first task, and a scheduler that has a custom policy to schedule the second task.  
  
 [!CODE [concrt-scheduler-policy#1](../CodeSnippet/VS_Snippets_ConcRT/concrt-scheduler-policy#1)]  
  
 This example produces the following output.  
  
 **Default scheduler:**  
**...........................................................................done**  
**Scheduler that has a custom policy:**  
**...........................................................................done** Although both sets of tasks produce the same result, the version that uses a custom policy enables the task that prints the progress indicator to run at an elevated priority so that it behaves more responsively.  
  
## Compiling the Code  
 Copy the example code and paste it in a Visual Studio project, or paste it in a file that is named `scheduler-policy.cpp` and then run the following command in a Visual Studio Command Prompt window.  
  
 **cl.exe /EHsc scheduler-policy.cpp**  
  
## See Also  
 [Scheduler Policies](../vs140/Scheduler-Policies.md)   
 [How-to: Manage a Scheduler Instance](../vs140/How-to--Manage-a-Scheduler-Instance.md)   
 [How-to: Create Agents that Use Specific Scheduler Policies](../vs140/How-to--Create-Agents-that-Use-Specific-Scheduler-Policies.md)