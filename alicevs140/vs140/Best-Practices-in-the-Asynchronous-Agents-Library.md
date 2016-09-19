---
title: "Best Practices in the Asynchronous Agents Library"
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
ms.assetid: 85f52354-41eb-4b0d-98c5-f7344ee8a8cf
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Best Practices in the Asynchronous Agents Library
This document describes how to make effective use of the Asynchronous Agents Library. The Agents Library promotes an actor-based programming model and in-process message passing for coarse-grained dataflow and pipelining tasks.  
  
 For more information about the Agents Library, see [Asynchronous Agents Library](../vs140/Asynchronous-Agents-Library.md).  
  
##  <a name="top"></a> Sections  
 This document contains the following sections:  
  
-   [Use Agents to Isolate State](#isolation)  
  
-   [Use a Throttling Mechanism to Limit the Number of Messages in a Data Pipeline](#throttling)  
  
-   [Do Not Perform Fine-Grained Work in a Data Pipeline](#fine-grained)  
  
-   [Do Not Pass Large Message Payloads by Value](#large-payloads)  
  
-   [Use shared_ptr in a Data Network When Ownership Is Undefined](#ownership)  
  
##  <a name="isolation"></a> Use Agents to Isolate State  
 The Agents Library provides alternatives to shared state by letting you connect isolated components through an asynchronous message-passing mechanism. Asynchronous agents are most effective when they isolate their internal state from other components. By isolating state, multiple components do not typically act on shared data. State isolation can enable your application to scale because it reduces contention on shared memory. State isolation also reduces the chance of deadlock and race conditions because components do not have to synchronize access to shared data.  
  
 You typically isolate state in an agent by holding data members in the `private` or `protected` sections of the agent class and by using message buffers to communicate state changes. The following example shows the `basic_agent` class, which derives from [concurrency::agent](../vs140/agent-Class.md). The `basic_agent` class uses two message buffers to communicate with external components. One message buffer holds incoming messages; the other message buffer holds outgoing messages.  
  
 [!CODE [concrt-simple-agent#1](../CodeSnippet/VS_Snippets_ConcRT/concrt-simple-agent#1)]  
  
 For complete examples about how to define and use agents, see [Walkthrough: Creating an Agent-Based Application](../vs140/Walkthrough--Creating-an-Agent-Based-Application.md) and [Walkthrough: Creating a Dataflow Agent](../vs140/Walkthrough--Creating-a-Dataflow-Agent.md).  
  
 [[Top](#top)]  
  
##  <a name="throttling"></a> Use a Throttling Mechanism to Limit the Number of Messages in a Data Pipeline  
 Many message-buffer types, such as [concurrency::unbounded_buffer](../vs140/unbounded_buffer-Class.md), can hold an unlimited number of messages. When a message producer sends messages to a data pipeline faster than the consumer can process these messages, the application can enter a low-memory or out-of-memory state. You can use a throttling mechanism, for example, a semaphore, to limit the number of messages that are concurrently active in a data pipeline.  
  
 The following basic example demonstrates how to use a semaphore to limit the number of messages in a data pipeline. The data pipeline uses the [concurrency::wait](../vs140/wait-Function.md) function to simulate an operation that takes at least 100 milliseconds. Because the sender produces messages faster than the consumer can process those messages, this example defines the `semaphore` class to enable the application to limit the number of active messages.  
  
 [!CODE [concrt-message-throttling#1](../CodeSnippet/VS_Snippets_ConcRT/concrt-message-throttling#1)]  
  
 The `semaphore` object limits the pipeline to process at most two messages at the same time.  
  
 The producer in this example sends relatively few messages to the consumer. Therefore, this example does not demonstrate a potential low-memory or out-of-memory condition. However, this mechanism is useful when a data pipeline contains a relatively high number of messages.  
  
 For more information about how to create the semaphore class that is used in this example, see [How to: Use the Context Class to Implement a Cooperative Semaphore](../vs140/How-to--Use-the-Context-Class-to-Implement-a-Cooperative-Semaphore.md).  
  
 [[Top](#top)]  
  
##  <a name="fine-grained"></a> Do Not Perform Fine-Grained Work in a Data Pipeline  
 The Agents Library is most useful when the work that is performed by a data pipeline is fairly coarse-grained. For example, one application component might read data from a file or a network connection and occasionally send that data to another component. The protocol that the Agents Library uses to propagate messages causes the message-passing mechanism to have more overhead than the task parallel constructs that are provided by the [Parallel Patterns Library](../vs140/Parallel-Patterns-Library--PPL-.md) (PPL). Therefore, make sure that the work that is performed by a data pipeline is long enough to offset this overhead.  
  
 Although a data pipeline is most effective when its tasks are coarse-grained, each stage of the data pipeline can use PPL constructs such as task groups and parallel algorithms to perform more fine-grained work. For an example of a coarse-grained data network that uses fine-grained parallelism at each processing stage, see [Walkthrough: Creating an Image-Processing Network](../vs140/Walkthrough--Creating-an-Image-Processing-Network.md).  
  
 [[Top](#top)]  
  
##  <a name="large-payloads"></a> Do Not Pass Large Message Payloads by Value  
 In some cases, the runtime creates a copy of every message that it passes from one message buffer to another message buffer. For example, the [concurrency::overwrite_buffer](../vs140/overwrite_buffer-Class.md) class offers a copy of every message that it receives to each of its targets. The runtime also creates a copy of the message data when you use message-passing functions such as [concurrency::send](../vs140/send-Function.md) and [concurrency::receive](../vs140/receive-Function.md) to write messages to and read messages from a message buffer. Although this mechanism helps eliminate the risk of concurrently writing to shared data, it could lead to poor memory performance when the message payload is relatively large.  
  
 You can use pointers or references to improve memory performance when you pass messages that have a large payload. The following example compares passing large messages by value to passing pointers to the same message type. The example defines two agent types, `producer` and `consumer`, that act on `message_data` objects. The example compares the time that is required for the producer to send several `message_data` objects to the consumer to the time that is required for the producer agent to send several pointers to `message_data` objects to the consumer.  
  
 [!CODE [concrt-message-payloads#1](../CodeSnippet/VS_Snippets_ConcRT/concrt-message-payloads#1)]  
  
 This example produces the following sample output:  
  
 **Using message_data...**  
**took 437ms.**  
**Using message_data\*...**  
**took 47ms.** The version that uses pointers performs better because it eliminates the requirement for the runtime to create a full copy of every `message_data` object that it passes from the producer to the consumer.  
  
 [[Top](#top)]  
  
##  <a name="ownership"></a> Use shared_ptr in a Data Network When Ownership Is Undefined  
 When you send messages by pointer through a message-passing pipeline or network, you typically allocate the memory for each message at the front of the network and free that memory at the end of the network. Although this mechanism frequently works well, there are cases in which it is difficult or not possible to use it. For example, consider the case in which the data network contains multiple end nodes. In this case, there is no clear location to free the memory for the messages.  
  
 To solve this problem, you can use a mechanism, for example, [std::shared_ptr](../vs140/shared_ptr-Class.md), that enables a pointer to be owned by multiple components. When the final `shared_ptr` object that owns a resource is destroyed, the resource is also freed.  
  
 The following example demonstrates how to use `shared_ptr` to share pointer values among multiple message buffers. The example connects a [concurrency::overwrite_buffer](../vs140/overwrite_buffer-Class.md) object to three [concurrency::call](../vs140/call-Class.md) objects. The `overwrite_buffer` class offers messages to each of its targets. Because there are multiple owners of the data at the end of the data network, this example uses `shared_ptr` to enable each `call` object to share ownership of the messages.  
  
 [!CODE [concrt-message-sharing#1](../CodeSnippet/VS_Snippets_ConcRT/concrt-message-sharing#1)]  
  
 This example produces the following sample output:  
  
 **Creating resource 42...**  
**receiver1: received resource 42**  
**Creating resource 64...**  
**receiver2: received resource 42**  
**receiver1: received resource 64**  
**Destroying resource 42...**  
**receiver2: received resource 64**  
**Destroying resource 64...**   
## See Also  
 [Concurrency Runtime Best Practices](../vs140/Concurrency-Runtime-Best-Practices.md)   
 [Asynchronous Agents Library](../vs140/Asynchronous-Agents-Library.md)   
 [Walkthrough: Creating an Agent-Based Application](../vs140/Walkthrough--Creating-an-Agent-Based-Application.md)   
 [Walkthrough: Creating a Dataflow Agent](../vs140/Walkthrough--Creating-a-Dataflow-Agent.md)   
 [Walkthrough: Creating an Image-Processing Network](../vs140/Walkthrough--Creating-an-Image-Processing-Network.md)   
 [Best Practices in the Parallel Patterns Library](../vs140/Best-Practices-in-the-Parallel-Patterns-Library.md)   
 [General Best Practices in the Concurrency Runtime](../vs140/General-Best-Practices-in-the-Concurrency-Runtime.md)