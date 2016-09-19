---
title: "Cancellation in the PPL"
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
ms.assetid: baaef417-b2f9-470e-b8bd-9ed890725b35
caps.latest.revision: 30
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Cancellation in the PPL
This document explains the role of cancellation in the Parallel Patterns Library (PPL), how to cancel parallel work, and how to determine when parallel work is canceled.  
  
> [!NOTE]
>  The runtime uses exception handling to implement cancellation. Do not catch or handle these exceptions in your code. In addition, we recommend that you write exception-safe code in the function bodies for your tasks. For instance, you can use the *Resource Acquisition Is Initialization* (RAII) pattern to ensure that resources are correctly handled when an exception is thrown in the body of a task. For a complete example that uses the RAII pattern to clean up a resource in a cancelable task, see [Walkthrough: Removing Work from a User-Interface Thread](../vs140/Walkthrough--Removing-Work-from-a-User-Interface-Thread.md).  
  
## Key Points  
  
-   Cancellation is cooperative and involves coordination between the code that requests cancellation and the task that responds to cancellation.  
  
-   When possible, use cancellation tokens to cancel work. The [concurrency::cancellation_token](../vs140/cancellation_token-Class.md) class defines a cancellation token.  
  
-   When you use cancellation tokens, use the [concurrency::cancellation_token_source::cancel](../vs140/cancellation_token_source--cancel-Method.md) method to initiate cancellation and the [concurrency::cancel_current_task](../vs140/cancel_current_task-Function.md) function to respond to cancellation.  
  
-   Cancellation does not occur immediately. Although new work is not started if a task or task group is cancelled, active work must check for and respond to cancellation.  
  
-   A value-based continuation inherits the cancellation token of its antecedent task. A task-based continuation never inherits the token of its antecedent task.  
  
-   Use the [concurrency::cancellation_token::none](../vs140/cancellation_token--none-Method.md) method when you call a constructor or function that takes a `cancellation_token` object but you do not want the operation to be cancellable. Also, if you do not pass a cancellation token to the [concurrency::task](../vs140/task-Class--Concurrency-Runtime-.md) constructor or the [concurrency::create_task](../vs140/create_task-Function.md) function, that task is not cancellable.  
  
##  <a name="top"></a> In this Document  
  
-   [Parallel Work Trees](#trees)  
  
-   [Canceling Parallel Tasks](#tasks)  
  
    -   [Using a Cancellation Token to Cancel Parallel Work](#tokens)  
  
    -   [Using the cancel Method to Cancel Parallel Work](#cancel)  
  
    -   [Using Exceptions to Cancel Parallel Work](#exceptions)  
  
-   [Canceling Parallel Algorithms](#algorithms)  
  
-   [When Not to Use Cancellation](#when)  
  
##  <a name="trees"></a> Parallel Work Trees  
 The PPL uses tasks and task groups to manage fine-grained tasks and computations. You can nest task groups to form *trees* of parallel work. The following illustration shows a parallel work tree. In this illustration, `tg1` and `tg2` represent task groups; `t1`, `t2`, `t3`, `t4`, and `t5` represent the work that the task groups perform.  
  
 ![A parallel work tree](../vs140/media/ParallelWork_Trees.png "ParallelWork_Trees")  
  
 The following example shows the code that is required to create the tree in the illustration. In this example, `tg1` and `tg2` are [concurrency::structured_task_group](../vs140/structured_task_group-Class.md) objects; `t1`, `t2`, `t3`, `t4`, and `t5` are [concurrency::task_handle](../vs140/task_handle-Class.md) objects.  
  
 [!CODE [concrt-task-tree#1](../CodeSnippet/VS_Snippets_ConcRT/concrt-task-tree#1)]  
  
 You can also use the [concurrency::task_group](../vs140/task_group-Class.md) class to create a similar work tree. The [concurrency::task](../vs140/task-Class--Concurrency-Runtime-.md) class also supports the notion of a tree of work. However, a `task` tree is a dependency tree. In a `task` tree, future works completes after current work. In a task group tree, internal work completes before outer work. For more information about the differences between tasks and task groups, see [Task Parallelism (Concurrency Runtime)](../vs140/Task-Parallelism--Concurrency-Runtime-.md).  
  
 [[Top](#top)]  
  
##  <a name="tasks"></a> Canceling Parallel Tasks  
 There are multiple ways to cancel parallel work. The preferred way is to use a cancellation token. Task groups also support the [concurrency::task_group::cancel](../vs140/task_group--cancel-Method.md) method and the [concurrency::structured_task_group::cancel](../vs140/structured_task_group--cancel-Method.md) method. The final way is to throw an exception in the body of a task work function. No matter which method you choose, understand that cancellation does not occur immediately. Although new work is not started if a task or task group is cancelled, active work must check for and respond to cancellation.  
  
 For more examples that cancel parallel tasks, see [Walkthrough: Connecting Using Tasks and XML HTTP Request (IXHR2)](../vs140/Walkthrough--Connecting-Using-Tasks-and-XML-HTTP-Requests.md), [How to: Use Cancellation to Break from a Parallel Loop](../vs140/How-to--Use-Cancellation-to-Break-from-a-Parallel-Loop.md), and [How to: Use Exception Handling to Break from a Parallel Loop](../vs140/How-to--Use-Exception-Handling-to-Break-from-a-Parallel-Loop.md).  
  
###  <a name="tokens"></a> Using a Cancellation Token to Cancel Parallel Work  
 The `task`, `task_group`, and `structured_task_group` classes support cancellation through the use of cancellation tokens. The PPL defines the [concurrency::cancellation_token_source](../vs140/cancellation_token_source-Class.md) and [concurrency::cancellation_token](../vs140/cancellation_token-Class.md) classes for this purpose. When you use a cancellation token to cancel work, the runtime does not start new work that subscribes to that token. Work that is already active can monitor its cancellation token and stop when it can.  
  
 To initiate cancellation, call the [concurrency::cancellation_token_source::cancel](../vs140/cancellation_token_source--cancel-Method.md) method. You respond to cancellation in these ways:  
  
-   For `task` objects, use the [concurrency::cancel_current_task](../vs140/cancel_current_task-Function.md) function. `cancel_current_task` cancels the current task and any of its value-based continuations. (It does not cancel the cancellation *token* that is associated with the task or its continuations.)  
  
-   For task groups and parallel algorithms, use the [concurrency::is_current_task_group_canceling](../vs140/is_current_task_group_canceling-Function.md) function to detect cancellation and return as soon as possible from the task body when this function returns `true`. (Do not call `cancel_current_task` from a task group.)  
  
 The following example shows the first basic pattern for task cancellation. The task body occasionally checks for cancellation inside a loop.  
  
 [!CODE [concrt-task-basic-cancellation#1](../CodeSnippet/VS_Snippets_ConcRT/concrt-task-basic-cancellation#1)]  
  
 The `cancel_current_task` function throws; therefore, you do not need to explicitly return from the current loop or function.  
  
> [!TIP]
>  Alternatively, you can call the [concurrency::interruption_point](../vs140/interruption_point-Function.md) function instead of `cancel_current_task`.  
  
 It is important to call `cancel_current_task` when you respond to cancellation because it transitions the task to the canceled state. If you return early instead of calling `cancel_current_task`, the operation transitions to the completed state and any value-based continuations are run.  
  
> [!CAUTION]
>  Never throw `task_canceled` from your code. Call `cancel_current_task` instead.  
  
 When a task ends in the canceled state, the [concurrency::task::get](../vs140/task--get-Method.md) method throws [concurrency::task_canceled](../vs140/task_canceled-Class.md). (Conversely, [concurrency::task::wait](../vs140/task--wait-Method.md) returns [task_status::canceled](../vs140/task_group_status-Enumeration.md) and does not throw.) The following example illustrates this behavior for a task-based continuation. A task-based continuation is always called, even when the antecedent task is canceled.  
  
 [!CODE [concrt-task-canceled#1](../CodeSnippet/VS_Snippets_ConcRT/concrt-task-canceled#1)]  
  
 Because value-based continuations inherit the token of their antecedent task unless they were created with an explicit token, the continuations immediately enter the canceled state even when the antecedent task is still executing. Therefore, any exception that is thrown by the antecedent task after cancellation is not propagated to the continuation tasks. Cancellation always overrides the state of the antecedent task. The following example resembles the previous, but illustrates the behavior for a value-based continuation.  
  
 [!CODE [concrt-task-canceled#2](../CodeSnippet/VS_Snippets_ConcRT/concrt-task-canceled#2)]  
  
> [!CAUTION]
>  If you do not pass a cancellation token to the `task` constructor or the [concurrency::create_task](../vs140/create_task-Function.md) function, that task is not cancellable. In addition, you must pass the same cancellation token to the constructor of any nested tasks (that is, tasks that are created in the body of another task) to cancel all tasks simultaneously.  
  
 You might want to run arbitrary code when a cancellation token is canceled. For example, if your user chooses a **Cancel** button on the user interface to cancel the operation, you could disable that button until the user starts another operation. The following example shows how to use the [concurrency::cancellation_token::register_callback](../vs140/cancellation_token--register_callback-Method.md) method to register a callback function that runs when a cancellation token is canceled.  
  
 [!CODE [concrt-task-cancellation-callback#1](../CodeSnippet/VS_Snippets_ConcRT/concrt-task-cancellation-callback#1)]  
  
 The document [Task Parallelism (Concurrency Runtime)](../vs140/Task-Parallelism--Concurrency-Runtime-.md) explains the difference between value-based and task-based continuations. If you do not provide a `cancellation_token` object to a continuation task, the continuation inherits the cancellation token from the antecedent task in the following ways:  
  
-   A value-based continuation always inherits the cancellation token of the antecedent task.  
  
-   A task-based continuation never inherits the cancellation token of the antecedent task. The only way to make a task-based continuation cancelable is to explicitly pass a cancellation token.  
  
 These behaviors are not affected by a faulted task (that is, one that throws an exception). In this case, a value-based continuation is cancelled; a task-based continuation is not cancelled.  
  
> [!CAUTION]
>  A task that is created in another task (in other words, a nested task) does not inherit the cancellation token of the parent task. Only a value-based continuation inherits the cancellation token of its antecedent task.  
  
> [!TIP]
>  Use the [concurrency::cancellation_token::none](../vs140/cancellation_token--none-Method.md) method when you call a constructor or function that takes a `cancellation_token` object and you do not want the operation to be cancellable.  
  
 You can also provide a cancellation token to the constructor of a `task_group` or `structured_task_group` object. An important aspect of this is that child task groups inherit this cancellation token. For an example that demonstrates this concept by using the [concurrency::run_with_cancellation_token](../vs140/run_with_cancellation_token-Function.md) function to run to call `parallel_for`, see [Canceling Parallel Algorithms](#algorithms) later in this document.  
  
 [[Top](#top)]  
  
#### Cancellation Tokens and Task Composition  
 The [concurrency:: HYPERLINK "http://msdn.microsoft.com/en-us/library/system.threading.tasks.task.whenall(v=VS.110).aspx" when_all](../vs140/when_all-Function.md) and [concurrency::when_any](../vs140/when_all-Function.md) functions can help you compose multiple tasks to implement common patterns. This section describes how these functions work with cancellation tokens.  
  
 When you provide a cancellation token to either the `when_all` and `when_any` function, that function cancels only when that cancellation token is cancelled or when one of the participant tasks ends in a canceled state or throws an exception.  
  
 The `when_all` function inherits the cancellation token from each task that composes the overall operation when you do not provide a cancellation token to it. The task that is returned from `when_all` is canceled when any of these tokens are cancelled and at least one of the participant tasks has not yet started or is running. A similar behavior occurs when one of the tasks throws an exception – the task that is returned from `when_all` is immediately canceled with that exception.  
  
 The runtime chooses the cancellation token for the task that is returned from `when_any` function when that task completes. If none of the participant tasks finish in a completed state and one or more of the tasks throws an exception, one of the tasks that threw is chosen to complete the `when_any` and its token is chosen as the token for the final task. If more than one task finishes in the completed state, the task that is returned from `when_any` task ends in a completed state. The runtime tries to pick a completed task whose token is not canceled at the time of completion so that the task that is returned from `when_any` is not immediately canceled even though other executing tasks might complete at a later point.  
  
 [[Top](#top)]  
  
###  <a name="cancel"></a> Using the cancel Method to Cancel Parallel Work  
 The [concurrency::task_group::cancel](../vs140/task_group--cancel-Method.md) and [concurrency::structured_task_group::cancel](../vs140/structured_task_group--cancel-Method.md) methods set a task group to the canceled state. After you call `cancel`, the task group does not start future tasks. The `cancel` methods can be called by multiple child tasks. A canceled task causes the [concurrency::task_group::wait](../vs140/task_group--wait-Method.md) and [concurrency::structured_task_group::wait](../vs140/structured_task_group--wait-Method.md) methods to return [concurrency::canceled](../vs140/task_group_status-Enumeration.md).  
  
 If a task group is canceled, calls from each child task into the runtime can trigger an *interruption point*, which causes the runtime to throw and catch an internal exception type to cancel active tasks. The Concurrency Runtime does not define specific interruption points; they can occur in any call to the runtime. The runtime must handle the exceptions that it throws in order to perform cancellation. Therefore, do not handle unknown exceptions in the body of a task.  
  
 If a child task performs a time-consuming operation and does not call into the runtime, it must periodically check for cancellation and exit in a timely manner. The following example shows one way to determine when work is canceled. Task `t4` cancels the parent task group when it encounters an error. Task `t5` occasionally calls the `structured_task_group::is_canceling` method to check for cancellation. If the parent task group is canceled, task `t5` prints a message and exits.  
  
 [!CODE [concrt-task-tree#6](../CodeSnippet/VS_Snippets_ConcRT/concrt-task-tree#6)]  
  
 This example checks for cancellation on every 100<sup>th</sup> iteration of the task loop. The frequency with which you check for cancellation depends on the amount of work your task performs and how quickly you need for tasks to respond to cancellation.  
  
 If you do not have access to the parent task group object, call the [concurrency::is_current_task_group_canceling](../vs140/is_current_task_group_canceling-Function.md) function to determine whether the parent task group is canceled.  
  
 The `cancel` method only affects child tasks. For example, if you cancel the task group `tg1` in the illustration of the parallel work tree, all tasks in the tree (`t1`, `t2`, `t3`, `t4`, and `t5`) are affected. If you cancel the nested task group, `tg2`, only tasks `t4` and `t5` are affected.  
  
 When you call the `cancel` method, all child task groups are also canceled. However, cancellation does not affect any parents of the task group in a parallel work tree. The following examples show this by building on the parallel work tree illustration.  
  
 The first of these examples creates a work function for the task `t4`, which is a child of the task group `tg2`. The work function calls the function `work` in a loop. If any call to `work` fails, the task cancels its parent task group. This causes task group `tg2` to enter the canceled state, but it does not cancel task group `tg1`.  
  
 [!CODE [concrt-task-tree#2](../CodeSnippet/VS_Snippets_ConcRT/concrt-task-tree#2)]  
  
 This second example resembles the first one, except that the task cancels task group `tg1`. This affects all tasks in the tree (`t1`, `t2`, `t3`, `t4`, and `t5`).  
  
 [!CODE [concrt-task-tree#3](../CodeSnippet/VS_Snippets_ConcRT/concrt-task-tree#3)]  
  
 The `structured_task_group` class is not thread-safe. Therefore, a child task that calls a method of its parent `structured_task_group` object produces unspecified behavior. The exceptions to this rule are the `structured_task_group::cancel` and [concurrency::structured_task_group::is_canceling](../vs140/structured_task_group--is_canceling-Method.md) methods. A child task can call these methods to cancel the parent task group and check for cancellation.  
  
> [!CAUTION]
>  Although you can use a cancellation token to cancel work that is performed by a task group that runs as a child of a `task` object, you cannot use the `task_group::cancel` or `structured_task_group::cancel` methods to cancel `task` objects that run in a task group.  
  
 [[Top](#top)]  
  
###  <a name="exceptions"></a> Using Exceptions to Cancel Parallel Work  
 The use of cancellation tokens and the `cancel` method are more efficient than exception handling at canceling a parallel work tree. Cancellation tokens and the `cancel` method cancel a task and any child tasks in a top-down manner. Conversely, exception handling works in a bottom-up manner and must cancel each child task group independently as the exception propagates upward. The topic [Exception Handling in the Concurrency Runtime](../vs140/Exception-Handling-in-the-Concurrency-Runtime.md) explains how the Concurrency Runtime uses exceptions to communicate errors. However, not all exceptions indicate an error. For example, a search algorithm might cancel its associated task when it finds the result. However, as mentioned previously, exception handling is less efficient than using the `cancel` method to cancel parallel work.  
  
> [!CAUTION]
>  We recommend that you use exceptions to cancel parallel work only when necessary. Cancellation tokens and the task group `cancel` methods are more efficient and less prone to error.  
  
 When you throw an exception in the body of a work function that you pass to a task group, the runtime stores that exception and marshals the exception to the context that waits for the task group to finish. As with the `cancel` method, the runtime discards any tasks that have not yet started, and does not accept new tasks.  
  
 This third example resembles the second one, except that task `t4` throws an exception to cancel the task group `tg2`. This example uses a `try`-`catch` block to check for cancellation when the task group `tg2` waits for its child tasks to finish. Like the first example, this causes the task group `tg2` to enter the canceled state, but it does not cancel task group `tg1`.  
  
 [!CODE [concrt-task-tree#4](../CodeSnippet/VS_Snippets_ConcRT/concrt-task-tree#4)]  
  
 This fourth example uses exception handling to cancel the whole work tree. The example catches the exception when task group `tg1` waits for its child tasks to finish instead of when task group `tg2` waits for its child tasks. Like the second example, this causes both tasks groups in the tree, `tg1` and `tg2`, to enter the canceled state.  
  
 [!CODE [concrt-task-tree#5](../CodeSnippet/VS_Snippets_ConcRT/concrt-task-tree#5)]  
  
 Because the `task_group::wait` and `structured_task_group::wait` methods throw when a child task throws an exception, you do not receive a return value from them.  
  
 [[Top](#top)]  
  
##  <a name="algorithms"></a> Canceling Parallel Algorithms  
 Parallel algorithms in the PPL, for example, `parallel_for`, build on task groups. Therefore, you can use many of the same techniques to cancel a parallel algorithm.  
  
 The following examples illustrate several ways to cancel a parallel algorithm.  
  
 The following example uses the `run_with_cancellation_token` function to call the `parallel_for` algorithm. The `run_with_cancellation_token` function takes a cancellation token as an argument and calls the provided work function synchronously. Because parallel algorithms are built upon tasks, they inherit the cancellation token of the parent task. Therefore, `parallel_for` can respond to cancellation.  
  
 [!CODE [concrt-cancel-parallel-for#1](../CodeSnippet/VS_Snippets_ConcRT/concrt-cancel-parallel-for#1)]  
  
 The following example uses the [concurrency::structured_task_group::run_and_wait](../vs140/structured_task_group--run_and_wait-Method.md) method to call the `parallel_for` algorithm. The `structured_task_group::run_and_wait` method waits for the provided task to finish. The `structured_task_group` object enables the work function to cancel the task.  
  
 [!CODE [concrt-task-tree#7](../CodeSnippet/VS_Snippets_ConcRT/concrt-task-tree#7)]  
  
 This example produces the following output.  
  
 **The task group status is: canceled.** The following example uses exception handling to cancel a `parallel_for` loop. The runtime marshals the exception to the calling context.  
  
 [!CODE [concrt-task-tree#9](../CodeSnippet/VS_Snippets_ConcRT/concrt-task-tree#9)]  
  
 This example produces the following output.  
  
 **Caught 50** The following example uses a Boolean flag to coordinate cancellation in a `parallel_for` loop. Every task runs because this example does not use the `cancel` method or exception handling to cancel the overall set of tasks. Therefore, this technique can have more computational overhead than a cancelation mechanism.  
  
 [!CODE [concrt-task-tree#8](../CodeSnippet/VS_Snippets_ConcRT/concrt-task-tree#8)]  
  
 Each cancellation method has advantages over the others. Choose the method that fits your specific needs.  
  
 [[Top](#top)]  
  
##  <a name="when"></a> When Not to Use Cancellation  
 The use of cancellation is appropriate when each member of a group of related tasks can exit in a timely manner. However, there are some scenarios where cancellation may not be appropriate for your application. For example, because task cancellation is cooperative, the overall set of tasks will not cancel if any individual task is blocked. For example, if one task has not yet started, but it unblocks another active task, it will not start if the task group is canceled. This can cause deadlock to occur in your application. A second example of where the use of cancellation may not be appropriate is when a task is canceled, but its child task performs an important operation, such as freeing a resource. Because the overall set of tasks is canceled when the parent task is canceled, that operation will not execute. For an example that illustrates this point, see the [Understand how Cancellation and Exception Handling Affect Object Destruction](../vs140/Best-Practices-in-the-Parallel-Patterns-Library.md#object-destruction) section in the Best Practices in the Parallel Patterns Library topic.  
  
 [[Top](#top)]  
  
## Related Topics  
  
|Title|Description|  
|-----------|-----------------|  
|[How to: Write a Parallel Search Algorithm](../vs140/How-to--Use-Cancellation-to-Break-from-a-Parallel-Loop.md)|Shows how to use cancellation to implement a parallel search algorithm.|  
|[How to: Write a Search Algorithm for a Basic Tree Structure](../vs140/How-to--Use-Exception-Handling-to-Break-from-a-Parallel-Loop.md)|Shows how to use the `task_group` class to write a search algorithm for a basic tree structure.|  
|[Exception Handling in the Concurrency Runtime](../vs140/Exception-Handling-in-the-Concurrency-Runtime.md)|Describes how the runtime handles exceptions that are thrown by task groups, lightweight tasks, and asynchronous agents, and how to respond to exceptions in your applications.|  
|[Task Parallelism](../vs140/Task-Parallelism--Concurrency-Runtime-.md)|Describes how tasks relate to task groups and how you can use unstructured and structured tasks in your applications.|  
|[Parallel Algorithms](../vs140/Parallel-Algorithms.md)|Describes the parallel algorithms, which concurrently perform work on collections of data|  
|[Parallel Patterns Library (PPL)](../vs140/Parallel-Patterns-Library--PPL-.md)|Provides an overview of the Parallel Patterns Library.|  
  
## Reference  
 [task Class (Concurrency Runtime)](../vs140/task-Class--Concurrency-Runtime-.md)  
  
 [cancellation_token_source Class](../vs140/cancellation_token_source-Class.md)  
  
 [cancellation_token Class](../vs140/cancellation_token-Class.md)  
  
 [task_group Class](../vs140/task_group-Class.md)  
  
 [structured_task_group Class](../vs140/structured_task_group-Class.md)  
  
 [parallel_for Function](../vs140/parallel_for-Function.md)