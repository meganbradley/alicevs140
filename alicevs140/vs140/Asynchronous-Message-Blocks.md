---
title: "Asynchronous Message Blocks"
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
ms.assetid: 79c456c0-1692-480c-bb67-98f2434c1252
caps.latest.revision: 32
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Asynchronous Message Blocks
The Agents Library provides several message-block types that enable you to propagate messages among application components in a thread-safe manner. These message-block types are often used with the various message-passing routines, such as [concurrency::send](../vs140/send-Function.md), [concurrency::asend](../vs140/asend-Function.md), [concurrency::receive](../vs140/receive-Function.md), and [concurrency::try_receive](../vs140/try_receive-Function.md). For more information about the message passing routines that are defined by the Agents Library, see [Message Passing Functions](../vs140/Message-Passing-Functions.md).  
  
##  <a name="top"></a> Sections  
 This topic contains the following sections:  
  
-   [Sources and Targets](#sources_and_targets)  
  
-   [Message Propagation](#propagation)  
  
-   [Overview of Message Block Types](#overview)  
  
-   [unbounded_buffer Class](#unbounded_buffer)  
  
-   [overwrite_buffer Class](#overwrite_buffer)  
  
-   [single_assignment Class](#single_assignment)  
  
-   [call Class](#call)  
  
-   [transformer Class](#transformer)  
  
-   [choice Class](#choice)  
  
-   [join and multitype_join Classes](#join)  
  
-   [timer Class](#timer)  
  
-   [Message Filtering](#filtering)  
  
-   [Message Reservation](#reservation)  
  
##  <a name="sources_and_targets"></a> Sources and Targets  
 Sources and targets are two important participants in message passing. A *source* refers to an endpoint of communication that sends messages. A *target* refers to an endpoint of communication that receives messages. You can think of a source as an endpoint that you read from and a target as an endpoint that you write to. Applications connect sources and targets together to form *messaging networks*.  
  
 The Agents Library uses two abstract classes to represent sources and targets: [concurrency::ISource](../vs140/ISource-Class.md) and [concurrency::ITarget](../vs140/ITarget-Class.md). Message block types that act as sources derive from `ISource`; message block types that act as targets derive from `ITarget`. Message block types that act as sources and targets derive from both `ISource` and `ITarget`.  
  
 [[Top](#top)]  
  
##  <a name="propagation"></a> Message Propagation  
 *Message propagation* is the act of sending a message from one component to another. When a message block is offered a message, it can accept, decline, or postpone that message. Every message block type stores and transmits messages in different ways. For example, the `unbounded_buffer` class stores an unlimited number of messages, the `overwrite_buffer` class stores a single message at a time, and the transformer class stores an altered version of each message. These message block types are described in more detail later in this document.  
  
 When a message block accepts a message, it can optionally perform work and, if the message block is a source, pass the resulting message to another member of the network. A message block can use a filter function to decline messages that it does not want to receive. Filters are described in more detail later in this topic, in the section [Message Filtering](#filtering). A message block that postpones a message can reserve that message and consume it later. Message reservation is described in more detail later in this topic, in the section [Message Reservation](#reservation).  
  
 The Agents Library enables message blocks to asynchronously or synchronously pass messages. When you pass a message to a message block synchronously, for example, by using the `send` function, the runtime blocks the current context until the target block either accepts or rejects the message. When you pass a message to a message block asynchronously, for example, by using the `asend` function, the runtime offers the message to the target, and if the target accepts the message, the runtime schedules an asynchronous task that propagates the message to the receiver. The runtime uses lightweight tasks to propagate messages in a cooperative manner. For more information about lightweight tasks, see [Task Scheduler (Concurrency Runtime)](../vs140/Task-Scheduler--Concurrency-Runtime-.md).  
  
 Applications connect sources and targets together to form messaging networks. Typically, you link the network and call `send` or `asend` to pass data to the network. To connect a source message block to a target, call the [concurrency::ISource::link_target](../vs140/ISource--link_target-Method.md) method. To disconnect a source block from a target, call the [concurrency::ISource::unlink_target](../vs140/ISource--unlink_target-Method.md) method. To disconnect a source block from all of its targets, call the [concurrency::ISource::unlink_targets](../vs140/ISource--unlink_targets-Method.md) method. When one of the predefined message block types leaves scope or is destroyed, it automatically disconnects itself from any target blocks. Some message block types restrict the maximum number of targets that they can write to. The following section describes the restrictions that apply to the predefined message block types.  
  
 [[Top](#top)]  
  
##  <a name="overview"></a> Overview of Message Block Types  
 The following table briefly describes the role of the important message-block types.  
  
 [unbounded_buffer](#unbounded_buffer)  
 Stores a queue of messages.  
  
 [overwrite_buffer](#overwrite_buffer)  
 Stores one message that can be written to and read from multiple times.  
  
 [single_assignment](#single_assignment)  
 Stores one message that can be written to one time and read from multiple times.  
  
 [call](#call)  
 Performs work when it receives a message.  
  
 [transformer](#transformer)  
 Performs work when it receives data and sends the result of that work to another target block. The `transformer` class can act on different input and output types.  
  
 [choice](#choice)  
 Selects the first available message from a set of sources.  
  
 [join and multitype join](#join)  
 Wait for all messages to be received from a set of sources and then combine the messages into one message for another message block.  
  
 [timer](#timer)  
 Sends a message to a target block on a regular interval.  
  
 These message-block types have different characteristics that make them useful for different situations. These are some of the characteristics:  
  
-   *Propagation type*: Whether the message block acts as a source of data, a receiver of data, or both.  
  
-   *Message ordering*: Whether the message block maintains the original order in which messages are sent or received. Each predefined message block type maintains the original order in which it sends or receives messages.  
  
-   *Source count*: The maximum number of sources that the message block can read from.  
  
-   *Target count*: The maximum number of targets that the message block can write to.  
  
 The following table shows how these characteristics relate to the various message-block types.  
  
|Message block type|Propagation type (Source, Target, or Both)|Message ordering (Ordered or Unordered)|Source count|Target count|  
|------------------------|--------------------------------------------------|-----------------------------------------------|------------------|------------------|  
|`unbounded_buffer`|Both|Ordered|Unbounded|Unbounded|  
|`overwrite_buffer`|Both|Ordered|Unbounded|Unbounded|  
|`single_assignment`|Both|Ordered|Unbounded|Unbounded|  
|`call`|Target|Ordered|Unbounded|Not Applicable|  
|`transformer`|Both|Ordered|Unbounded|1|  
|`choice`|Both|Ordered|10|1|  
|`join`|Both|Ordered|Unbounded|1|  
|`multitype_join`|Both|Ordered|10|1|  
|`timer`|Source|Not Applicable|Not Applicable|1|  
  
 The following sections describe the message-block types in more detail.  
  
 [[Top](#top)]  
  
##  <a name="unbounded_buffer"></a> unbounded_buffer Class  
 The [concurrency::unbounded_buffer](../vs140/unbounded_buffer-Class.md) class represents a general-purpose asynchronous messaging structure. This class stores a first in, first out (FIFO) queue of messages that can be written to by multiple sources or read from by multiple targets. When a target receives a message from an `unbounded_buffer` object, that message is removed from the message queue. Therefore, although an `unbounded_buffer` object can have multiple targets, only one target will receive each message. The `unbounded_buffer` class is useful when you want to pass multiple messages to another component, and that component must receive each message.  
  
### Example  
 The following example shows the basic structure of how to work with the `unbounded_buffer` class. This example sends three values to an `unbounded_buffer` object and then reads those values back from the same object.  
  
 [!CODE [concrt-unbounded_buffer-structure#1](../CodeSnippet/VS_Snippets_ConcRT/concrt-unbounded_buffer-structure#1)]  
  
 This example produces the following output:  
  
 **334455** For a complete example that shows how to use the `unbounded_buffer` class, see [How to: Implement Various Producer-Consumer Patterns](../vs140/How-to--Implement-Various-Producer-Consumer-Patterns.md).  
  
 [[Top](#top)]  
  
##  <a name="overwrite_buffer"></a> overwrite_buffer Class  
 The [concurrency::overwrite_buffer](../vs140/overwrite_buffer-Class.md) class resembles the `unbounded_buffer` class, except that an `overwrite_buffer` object stores just one message. In addition, when a target receives a message from an `overwrite_buffer` object, that message is not removed from the buffer. Therefore, multiple targets receive a copy of the message.  
  
 The `overwrite_buffer` class is useful when you want to pass multiple messages to another component, but that component needs only the most recent value. This class is also useful when you want to broadcast a message to multiple components.  
  
### Example  
 The following example shows the basic structure of how to work with the `overwrite_buffer` class. This example sends three values to an `overwrite _buffer` object and then reads the current value from the same object three times. This example is similar to the example for the `unbounded_buffer` class. However, the `overwrite_buffer` class stores just one message. In addition, the runtime does not remove the message from an `overwrite_buffer` object after it is read.  
  
 [!CODE [concrt-overwrite_buffer-structure#1](../CodeSnippet/VS_Snippets_ConcRT/concrt-overwrite_buffer-structure#1)]  
  
 This example produces the following output:  
  
 **555555** For a complete example that shows how to use the `overwrite_buffer` class, see [How to: Implement Various Producer-Consumer Patterns](../vs140/How-to--Implement-Various-Producer-Consumer-Patterns.md).  
  
 [[Top](#top)]  
  
##  <a name="single_assignment"></a> single_assignment Class  
 The [concurrency::single_assignment](../vs140/single_assignment-Class.md) class resembles the `overwrite_buffer` class, except that a `single_assignment` object can be written to one time only. Like the `overwrite_buffer` class, when a target receives a message from a `single_assignment` object, that message is not removed from that object. Therefore, multiple targets receive a copy of the message. The `single_assignment` class is useful when you want to broadcast one message to multiple components.  
  
### Example  
 The following example shows the basic structure of how to work with the `single_assignment` class. This example sends three values to a `single_assignment` object and then reads the current value from the same object three times. This example is similar to the example for the `overwrite_buffer` class. Although both the `overwrite_buffer` and `single_assignment` classes store a single message, the `single_assignment` class can be written to one time only.  
  
 [!CODE [concrt-single_assignment-structure#1](../CodeSnippet/VS_Snippets_ConcRT/concrt-single_assignment-structure#1)]  
  
 This example produces the following output:  
  
 **333333** For a complete example that shows how to use the `single_assignment` class, see [Walkthrough: Implementing Futures](../vs140/Walkthrough--Implementing-Futures.md).  
  
 [[Top](#top)]  
  
##  <a name="call"></a> call Class  
 The [concurrency::call](../vs140/call-Class.md) class acts as a message receiver that performs a work function when it receives data. This work function can be a lambda expression, a function object, or a function pointer. A `call` object behaves differently than an ordinary function call because it acts in parallel to other components that send messages to it. If a `call` object is performing work when it receives a message, it adds that message to a queue. Every `call` object processes queued messages in the order in which they are received.  
  
### Example  
 The following example shows the basic structure of how to work with the `call` class. This example creates a `call` object that prints each value that it receives to the console. The example then sends three values to the `call` object. Because the `call` object processes messages on a separate thread, this example also uses a counter variable and an [event](../vs140/event-Class.md) object to ensure that the `call` object processes all messages before the `wmain` function returns.  
  
 [!CODE [concrt-call-structure#1](../CodeSnippet/VS_Snippets_ConcRT/concrt-call-structure#1)]  
  
 This example produces the following output:  
  
 **334455** For a complete example that shows how to use the `call` class, see [How to: Use the call Class](../vs140/How-to--Provide-Work-Functions-to-the-call-and-transformer-Classes.md).  
  
 [[Top](#top)]  
  
##  <a name="transformer"></a> transformer Class  
 The [concurrency::transformer](../vs140/transformer-Class.md) class acts as both a message receiver and as a message sender. The `transformer` class resembles the `call` class because it performs a user-defined work function when it receives data. However, the `transformer` class also sends the result of the work function to receiver objects. Like a `call` object, a `transformer` object acts in parallel to other components that send messages to it. If a `transformer` object is performing work when it receives a message, it adds that message to a queue. Every `transformer` object processes its queued messages in the order in which they are received.  
  
 The `transformer` class sends its message to one target. If you set the `_PTarget` parameter in the constructor to `NULL`, you can later specify the target by calling the [concurrency::link_target](../vs140/source_block--link_target-Method.md) method.  
  
 Unlike all other asynchronous message block types that are provided by the Agents Library, the `transformer` class can act on different input and output types. This ability to transform data from one type to another makes the `transformer` class a key component in many concurrent networks. In addition, you can add more fine-grained parallel functionality in the work function of a `transformer` object.  
  
### Example  
 The following example shows the basic structure of how to work with the `transformer` class. This example creates a `transformer` object that multiples each input `int` value by 0.33 in order to produce a `double` value as output. The example then receives the transformed values from the same `transformer` object and prints them to the console.  
  
 [!CODE [concrt-transformer-structure#1](../CodeSnippet/VS_Snippets_ConcRT/concrt-transformer-structure#1)]  
  
 This example produces the following output:  
  
 **10.8914.5218.15** For a complete example that shows how to use the `transformer` class, see [How to: Use transformer in a Data Pipeline](../vs140/How-to--Use-transformer-in-a-Data-Pipeline.md).  
  
 [[Top](#top)]  
  
##  <a name="choice"></a> choice Class  
 The [concurrency::choice](../vs140/choice-Class.md) class selects the first available message from a set of sources. The `choice` class represents a control-flow mechanism instead of a dataflow mechanism (the topic [Asynchronous Agents Library](../vs140/Asynchronous-Agents-Library.md) describes the differences between dataflow and control-flow).  
  
 Reading from a choice object resembles calling the Windows API function `WaitForMultipleObjects` when it has the `bWaitAll` parameter set to `FALSE`. However, the `choice` class binds data to the event itself instead of to an external synchronization object.  
  
 Typically, you use the `choice` class together with the [concurrency::receive](../vs140/receive-Function.md) function to drive control-flow in your application. Use the `choice` class when you have to select among message buffers that have different types. Use the `single_assignment` class when you have to select among message buffers that have the same type.  
  
 The order in which you link sources to a `choice` object is important because it can determine which message is selected. For example, consider the case where you link multiple message buffers that already contain a message to a `choice` object. The `choice` object selects the message from the first source that it is linked to. After you link all sources, the `choice` object preserves the order in which each source receives a message.  
  
### Example  
 The following example shows the basic structure of how to work with the `choice` class. This example uses the [concurrency::make_choice](../vs140/make_choice-Function.md) function to create a `choice` object that selects among three message blocks. The example then computes various Fibonacci numbers and stores each result in a different message block. The example then prints to the console a message that is based on the operation that finished first.  
  
 [!CODE [concrt-choice-structure#1](../CodeSnippet/VS_Snippets_ConcRT/concrt-choice-structure#1)]  
  
 This example produces the following sample output:  
  
 **fib35 received its value first. Result = 9227465** Because the task that computes the 35<sup>th</sup> Fibonacci number is not guaranteed to finish first, the output of this example can vary.  
  
 This example uses the [concurrency::parallel_invoke](../vs140/parallel_invoke-Function.md) algorithm to compute the Fibonacci numbers in parallel. For more information about `parallel_invoke`, see [Parallel Algorithms](../vs140/Parallel-Algorithms.md).  
  
 For a complete example that shows how to use the `choice` class, see [How to: Select Among Completed Tasks](../vs140/How-to--Select-Among-Completed-Tasks.md).  
  
 [[Top](#top)]  
  
##  <a name="join"></a> join and multitype_join Classes  
 The [concurrency::join](../vs140/join-Class.md) and [concurrency::multitype_join](../vs140/multitype_join-Class.md) classes let you wait for each member of a set of sources to receive a message. The `join` class acts on source objects that have a common message type. The `multitype_join` class acts on source objects that can have different message types.  
  
 Reading from a `join` or `multitype_join` object resembles calling the Windows API function `WaitForMultipleObjects` when it has the `bWaitAll` parameter set to `TRUE`. However, just like a `choice` object, `join` and `multitype_join` objects use an event mechanism that binds data to the event itself instead of to an external synchronization object.  
  
 Reading from a `join` object produces a [std::vector](../vs140/vector-Class.md) object. Reading from a `multitype_join` object produces a [std::tuple](../vs140/tuple-Class.md) object. Elements appear in these objects in the same order as their corresponding source buffers are linked to the `join` or `multitype_join` object. Because the order in which you link source buffers to a `join` or `multitype_join` object is associated with the order of elements in the resulting `vector` or `tuple` object, we recommend that you do not unlink an existing source buffer from a join. Doing so can result in unspecified behavior.  
  
### Greedy Versus Non-Greedy Joins  
 The `join` and `multitype_join` classes support the concept of greedy and non-greedy joins. A *greedy join* accepts a message from each of its sources as messages become available until all message are available. A *non-greedy join* receives messages in two phases. First, a non-greedy join waits until it is offered a message from each of its sources. Second, after all source messages are available, a non-greedy join attempts to reserve each of those messages. If it can reserve each message, it consumes all messages and propagates them to its target. Otherwise, it releases, or cancels, the message reservations and again waits for each source to receive a message.  
  
 Greedy joins perform better than non-greedy joins because they accept messages immediately. However, in rare cases, greedy joins can lead to deadlocks. Use a non-greedy join when you have multiple joins that contain one or more shared source objects.  
  
### Example  
 The following example shows the basic structure of how to work with the `join` class. This example uses the [concurrency::make_join](../vs140/make_join-Function.md) function to create a `join` object that receives from three `single_assignment` objects. This example computes various Fibonacci numbers, stores each result in a different `single_assignment` object, and then prints to the console each result that the `join` object holds. This example is similar to the example for the `choice` class, except that the `join` class waits for all source message blocks to receive a message.  
  
 [!CODE [concrt-join-structure#1](../CodeSnippet/VS_Snippets_ConcRT/concrt-join-structure#1)]  
  
 This example produces the following output:  
  
 **fib35 = 9227465fib37 = 24157817half_of_fib42 = 1.33957e+008** This example uses the [concurrency::parallel_invoke](../vs140/parallel_invoke-Function.md) algorithm to compute the Fibonacci numbers in parallel. For more information about `parallel_invoke`, see [Parallel Algorithms](../vs140/Parallel-Algorithms.md).  
  
 For complete examples that show how to use the `join` class, see [How to: Select Among Completed Tasks](../vs140/How-to--Select-Among-Completed-Tasks.md) and [Walkthrough: Using join to Prevent Deadlock](../vs140/Walkthrough--Using-join-to-Prevent-Deadlock.md).  
  
 [[Top](#top)]  
  
##  <a name="timer"></a> timer Class  
 The [concurrency::timer](../vs140/timer-Class.md) class acts as a message source. A `timer` object sends a message to a target after a specified period of time has elapsed. The `timer` class is useful when you must delay sending a message or you want to send a message at a regular interval.  
  
 The `timer` class sends its message to just one target. If you set the `_PTarget` parameter in the constructor to `NULL`, you can later specify the target by calling the [concurrency::ISource::link_target](../vs140/source_block--link_target-Method.md) method.  
  
 A `timer` object can be repeating or non-repeating. To create a repeating timer, pass `true` for the `_Repeating` parameter when you call the constructor. Otherwise, pass `false` for the `_Repeating` parameter to create a non-repeating timer. If the timer is repeating, it sends the same message to its target after each interval.  
  
 The Agents Library creates `timer` objects in the non-started state. To start a timer object, call the [concurrency::timer::start](../vs140/timer--start-Method.md) method. To stop a `timer` object, destroy the object or call the [concurrency::timer::stop](../vs140/timer--stop-Method.md) method. To pause a repeating timer, call the [concurrency::timer::pause](../vs140/timer--pause-Method.md) method.  
  
### Example  
 The following example shows the basic structure of how to work with the `timer` class. The example uses `timer` and `call` objects to report the progress of a lengthy operation.  
  
 [!CODE [concrt-timer-structure#1](../CodeSnippet/VS_Snippets_ConcRT/concrt-timer-structure#1)]  
  
 This example produces the following sample output:  
  
 **Computing fib(42)..................................................result is 267914296** For a complete example that shows how to use the `timer` class, see [How to: Send a Message at a Regular Interval](../vs140/How-to--Send-a-Message-at-a-Regular-Interval.md).  
  
 [[Top](#top)]  
  
##  <a name="filtering"></a> Message Filtering  
 When you create a message block object, you can supply a *filter function* that determines whether the message block accepts or rejects a message. A filter function is a useful way to guarantee that a message block receives only certain values.  
  
 The following example shows how to create an `unbounded_buffer` object that uses a filter function to accept only even numbers. The `unbounded_buffer` object rejects odd numbers, and therefore does not propagate odd numbers to its target blocks.  
  
 [!CODE [concrt-filter-function#1](../CodeSnippet/VS_Snippets_ConcRT/concrt-filter-function#1)]  
  
 This example produces the following output:  
  
 **0 2 4 6 8** A filter function can be a lambda function, a function pointer, or a function object. Every filter function takes one of the following forms.  
  
 **bool (_Type)**  
**bool (_Type const &)** To eliminate the unnecessary copying of data, use the second form when you have an aggregate type that is propagated by value.  
  
 Message filtering supports the *dataflow* programming model, in which components perform computations when they receive data. For examples that use filter functions to control the flow of data in a message passing network, see [How to: Use a Message Block Filter to Improve Performance](../vs140/How-to--Use-a-Message-Block-Filter.md), [Walkthrough: Creating a Dataflow Agent](../vs140/Walkthrough--Creating-a-Dataflow-Agent.md), and [Walkthrough: Creating an Image-Processing Network](../vs140/Walkthrough--Creating-an-Image-Processing-Network.md).  
  
 [[Top](#top)]  
  
##  <a name="reservation"></a> Message Reservation  
 *Message reservation* enables a message block to reserve a message for later use. Typically, message reservation is not used directly. However, understanding message reservation can help you better understand the behavior of some of the predefined message block types.  
  
 Consider non-greedy and greedy joins. Both of these use message reservation to reserve messages for later use. A described earlier, a non-greedy join receives messages in two phases. During the first phase, a non-greedy `join` object waits for each of its sources to receive a message. A non-greedy join then attempts to reserve each of those messages. If it can reserve each message, it consumes all messages and propagates them to its target. Otherwise, it releases, or cancels, the message reservations and again waits for each source to receive a message.  
  
 A greedy join, which also reads input messages from a number of sources, uses message reservation to read additional messages while it waits to receive a message from each source. For example, consider a greedy join that receives messages from message blocks `A` and `B`. If the greedy join receives two messages from B but has not yet received a message from `A`, the greedy join saves the unique message identifier for the second message from `B`. After the greedy join receives a message from `A` and propagates out these messages, it uses the saved message identifier to see if the second message from `B` is still available.  
  
 You can use message reservation when you implement your own custom message block types. For an example about how to create a custom message block type, see [Walkthrough: Creating a Custom Message Block](../vs140/Walkthrough--Creating-a-Custom-Message-Block.md).  
  
 [[Top](#top)]  
  
## See Also  
 [Asynchronous Agents Library](../vs140/Asynchronous-Agents-Library.md)