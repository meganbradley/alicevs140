---
title: "Asynchronous Agents"
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
ms.assetid: 6cf6ccc6-87f1-4e14-af15-ea8ba58fef1a
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Asynchronous Agents
An *asynchronous agent* (or just *agent*) is an application component that works asynchronously with other agents to solve larger computing tasks. Think of an agent as a task that has a set life cycle. For example, one agent might read data from an input/output device (such as the keyboard, a file on disk, or a network connection) and another agent might perform action on that data as it becomes available. The first agent uses message passing to inform the second agent that more data is available. The Concurrency Runtime task scheduler provides an efficient mechanism to enable agents to block and yield cooperatively without requiring less efficient preemption.  
  
 The Agents Library defines the [concurrency::agent](../vs140/agent-Class.md) class to represent an asynchronous agent. `agent` is an abstract class that declares the virtual method [concurrency::agent::run](../vs140/agent--run-Method.md). The `run` method executes the task that is performed by the agent. Because `run` is abstract, you must implement this method in every class that you derive from `agent`.  
  
## Agent Life Cycle  
 Agents have a set life cycle. The [concurrency::agent_status](../vs140/agent_status-Enumeration.md) enumeration defines the various states of an agent. The following illustration is a state diagram that shows how agents progress from one state to another. In this illustration, solid lines represent methods that you call from your application; dotted lines represent methods that are called from the runtime.  
  
 ![Agent State Diagram](../vs140/media/AgentState.png "AgentState")  
  
 The following table describes each state in the `agent_status` enumeration.  
  
|Agent State|Description|  
|-----------------|-----------------|  
|`agent_created`|The agent has not been scheduled for execution.|  
|`agent_runnable`|The runtime is scheduling the agent for execution.|  
|`agent_started`|The agent has started and is running.|  
|`agent_done`|The agent finished.|  
|`agent_canceled`|The agent was canceled before it entered the `started` state.|  
  
 `agent_created` is the initial state of an agent, `agent_runnable` and `agent_started` are the active states, and `agent_done` and `agent_canceled` are the terminal states.  
  
 Use the [concurrency::agent::status](../vs140/agent--status-Method.md) method to retrieve the current state of an `agent` object. Although the `status` method is concurrency-safe, the state of the agent can change by the time the `status` method returns. For example, an agent could be in the `agent_started` state when you call the `status` method, but moved to the `agent_done` state just after the `status` method returns.  
  
## Methods and Features  
 The following table shows some of the important methods that belong to the `agent` class. For more information about all of the `agent` class methods, see [agent Class](../vs140/agent-Class.md).  
  
|Method|Description|  
|------------|-----------------|  
|[start](../vs140/agent--start-Method.md)|Schedules the `agent` object for execution and sets it to the `agent_runnable` state.|  
|[run](../vs140/agent--run-Method.md)|Executes the task that is to be performed by the `agent` object.|  
|[done](../vs140/agent--done-Method.md)|Moves an agent to the `agent_done` state.|  
|[cancel](../vs140/agent--cancel-Method.md)|If the agent was not started, this method cancels execution of the agent and sets it to the `agent_canceled` state.|  
|[status](../vs140/agent--status-Method.md)|Retrieves the current state of the `agent` object.|  
|[wait](../vs140/agent--wait-Method.md)|Waits for the `agent` object to enter the `agent_done` or `agent_canceled` state.|  
|[wait_for_all](../vs140/agent--wait_for_all-Method.md)|Waits for all provided `agent` objects to enter the `agent_done` or `agent_canceled` state.|  
|[wait_for_one](../vs140/agent--wait_for_one-Method.md)|Waits for at least one of the provided `agent` objects to enter the `agent_done` or `agent_canceled` state.|  
  
 After you create an agent object, call the [concurrency::agent::start](../vs140/agent--start-Method.md) method to schedule it for execution. The runtime calls the `run` method after it schedules the agent and sets it to the `agent_runnable` state.  
  
 The runtime does not manage exceptions that are thrown by asynchronous agents. For more information about exception handling and agents, see [Exception Handling in the Concurrency Runtime](../vs140/Exception-Handling-in-the-Concurrency-Runtime.md).  
  
## Example  
 For an example that shows how to create a basic agent-based application, see [Walkthrough: Creating an Agent-Based Application](../vs140/Walkthrough--Creating-an-Agent-Based-Application.md).  
  
## See Also  
 [Asynchronous Agents Library](../vs140/Asynchronous-Agents-Library.md)