---
title: "agent Class"
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
ms.assetid: 1b09e3d2-5e37-4966-b016-907ef1512456
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# agent Class
A class intended to be used as a base class for all independent agents. It is used to hide state from other agents and interact using message-passing.  
  
## Syntax  
  
```  
class agent;  
```  
  
## Members  
  
### Public Constructors  
  
|Name|Description|  
|----------|-----------------|  
|[agent::agent Constructor](#agent__agent_constructor)|Overloaded. Constructs an agent.|  
|[agent::~agent Destructor](#agent___dtoragent_destructor)|Destroys the agent.|  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[agent::cancel Method](#agent__cancel_method)|Moves an agent from either the                                         `agent_created` or                                         `agent_runnable` states to the                                         `agent_canceled` state.|  
|[agent::start Method](#agent__start_method)|Moves an agent from the                                         `agent_created` state to the                                         `agent_runnable` state, and schedules it for execution.|  
|[agent::status Method](#agent__status_method)|A synchronous source of status information from the agent.|  
|[agent::status_port Method](#agent__status_port_method)|An asynchronous source of status information from the agent.|  
|[agent::wait Method](#agent__wait_method)|Waits for an agent to complete its task.|  
|[agent::wait_for_all Method](#agent__wait_for_all_method)|Waits for all of the specified agents to complete their tasks.|  
|[agent::wait_for_one Method](#agent__wait_for_one_method)|Waits for any one of the specified agents to complete its task.|  
  
### Protected Methods  
  
|Name|Description|  
|----------|-----------------|  
|[agent::done Method](#agent__done_method)|Moves an agent into the                                         `agent_done` state, indicating that the agent has completed.|  
|[agent::run Method](#agent__run_method)|Represents the main task of an agent.                                         `run` should be overridden in a derived class, and specifies what the agent should do after it has been started.|  
  
## Remarks  
 For more information, see                 [Asynchronous Agents](../vs140/Asynchronous-Agents.md).  
  
## Inheritance Hierarchy  
 `agent`  
  
## Requirements  
 **Header:** agents.h  
  
 **Namespace:** concurrency  
  
##  <a name="agent__agent_constructor"></a>  agent::agent Constructor  
 Constructs an agent.  
  
```  
agent();  
  
agent(  
   Scheduler&                 _PScheduler  
);  
  
agent(  
   ScheduleGroup&                 _PGroup  
);  
```  
  
### Parameters  
 `_PScheduler`  
 The                                 `Scheduler` object within which the execution task of the agent is scheduled.  
  
 `_PGroup`  
 The                                 `ScheduleGroup` object within which the execution task of the agent is scheduled. The                                 `Scheduler` object used is implied by the schedule group.  
  
### Remarks  
 The runtime uses the default scheduler if you do not specify the                         `_PScheduler` or                         `_PGroup` parameters.  
  
##  <a name="agent___dtoragent_destructor"></a>  agent::~agent Destructor  
 Destroys the agent.  
  
```  
virtual ~agent();  
```  
  
### Remarks  
 It is an error to destroy an agent that is not in a terminal state (either                         `agent_done` or                         `agent_canceled`). This can be avoided by waiting for the agent to reach a terminal state in the destructor of a class that inherits from the                         `agent` class.  
  
##  <a name="agent__cancel_method"></a>  agent::cancel Method  
 Moves an agent from either the                 `agent_created` or                 `agent_runnable` states to the                 `agent_canceled` state.  
  
```  
bool cancel();  
```  
  
### Return Value  
 `true` if the agent was canceled,                         `false` otherwise. An agent cannot be canceled if it has already started running or has already completed.  
  
##  <a name="agent__done_method"></a>  agent::done Method  
 Moves an agent into the                 `agent_done` state, indicating that the agent has completed.  
  
```  
bool done();  
```  
  
### Return Value  
 `true` if the agent is moved to the                         `agent_done` state,                         `false` otherwise. An agent that has been canceled cannot be moved to the                         `agent_done` state.  
  
### Remarks  
 This method should be called at the end of the                         `run` method, when you know the execution of your agent has completed.  
  
##  <a name="agent__run_method"></a>  agent::run Method  
 Represents the main task of an agent.                 `run` should be overridden in a derived class, and specifies what the agent should do after it has been started.  
  
```  
virtual void run() = 0;  
```  
  
### Remarks  
 The agent status is changed to                         `agent_started` right before this method is invoked. The method should invoke                         `done` on the agent with an appropriate status before returning, and may not throw any exceptions.  
  
##  <a name="agent__start_method"></a>  agent::start Method  
 Moves an agent from the                 `agent_created` state to the                 `agent_runnable` state, and schedules it for execution.  
  
```  
bool start();  
```  
  
### Return Value  
 `true` if the agent started correctly,                         `false` otherwise. An agent that has been canceled cannot be started.  
  
##  <a name="agent__status_method"></a>  agent::status Method  
 A synchronous source of status information from the agent.  
  
```  
agent_status status();  
```  
  
### Return Value  
 Returns the current state of the agent. Note that this returned state could change immediately after being returned.  
  
##  <a name="agent__status_port_method"></a>  agent::status_port Method  
 An asynchronous source of status information from the agent.  
  
```  
ISource<agent_status> * status_port();  
```  
  
### Return Value  
 Returns a message source that can send messages about the current state of the agent.  
  
##  <a name="agent__wait_method"></a>  agent::wait Method  
 Waits for an agent to complete its task.  
  
```  
static agent_status __cdecl wait(  
   _Inout_ agent *                 _PAgent,  
   unsigned int                 _Timeout = COOPERATIVE_TIMEOUT_INFINITE  
);  
```  
  
### Parameters  
 `_PAgent`  
 A pointer to the agent to wait for.  
  
 `_Timeout`  
 The maximum time for which to wait, in milliseconds.  
  
### Return Value  
 The                         `agent_status` of the agent when the wait completes. This can either be                         `agent_canceled` or                         `agent_done`.  
  
### Remarks  
 An agent task is completed when the agent enters the                         `agent_canceled` or                         `agent_done` states.  
  
 If the parameter                         `_Timeout` has a value other than the constant                         `COOPERATIVE_TIMEOUT_INFINITE`, the exception                         [operation_timed_out](../vs140/operation_timed_out-Class.md) is thrown if the specified amount of time expires before the agent has completed its task.  
  
##  <a name="agent__wait_for_all_method"></a>  agent::wait_for_all Method  
 Waits for all of the specified agents to complete their tasks.  
  
```  
static void __cdecl wait_for_all(  
   size_t                 _Count,  
   _In_reads_(_Count) agent **                 _PAgents,  
   _Out_writes_opt_(_Count) agent_status *                 _PStatus = NULL,  
   unsigned int                 _Timeout = COOPERATIVE_TIMEOUT_INFINITE  
);  
```  
  
### Parameters  
 `_Count`  
 The number of agent pointers present in the array                                 `_PAgents`.  
  
 `_PAgents`  
 An array of pointers to the agents to wait for.  
  
 `_PStatus`  
 A pointer to an array of agent statuses. Each status value will represent the status of the corresponding agent when the method returns.  
  
 `_Timeout`  
 The maximum time for which to wait, in milliseconds.  
  
### Remarks  
 An agent task is completed when the agent enters the                         `agent_canceled` or                         `agent_done` states.  
  
 If the parameter                         `_Timeout` has a value other than the constant                         `COOPERATIVE_TIMEOUT_INFINITE`, the exception                         [operation_timed_out](../vs140/operation_timed_out-Class.md) is thrown if the specified amount of time expires before the agent has completed its task.  
  
##  <a name="agent__wait_for_one_method"></a>  agent::wait_for_one Method  
 Waits for any one of the specified agents to complete its task.  
  
```  
static void __cdecl wait_for_one(  
   size_t                 _Count,  
   _In_reads_(_Count) agent **                 _PAgents,  
   agent_status&                 _Status,  
   size_t&                 _Index,  
   unsigned int                 _Timeout = COOPERATIVE_TIMEOUT_INFINITE  
);  
```  
  
### Parameters  
 `_Count`  
 The number of agent pointers present in the array                                 `_PAgents`.  
  
 `_PAgents`  
 An array of pointers to the agents to wait for.  
  
 `_Status`  
 A reference to a variable where the agent status will be placed.  
  
 `_Index`  
 A reference to a variable where the agent index will be placed.  
  
 `_Timeout`  
 The maximum time for which to wait, in milliseconds.  
  
### Remarks  
 An agent task is completed when the agent enters the                         `agent_canceled` or                         `agent_done` states.  
  
 If the parameter                         `_Timeout` has a value other than the constant                         `COOPERATIVE_TIMEOUT_INFINITE`, the exception                         [operation_timed_out](../vs140/operation_timed_out-Class.md) is thrown if the specified amount of time expires before the agent has completed its task.  
  
## See Also  
 [concurrency Namespace](../vs140/concurrency-Namespace.md)