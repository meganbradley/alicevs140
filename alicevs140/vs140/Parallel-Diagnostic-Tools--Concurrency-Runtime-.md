---
title: "Parallel Diagnostic Tools (Concurrency Runtime)"
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
ms.assetid: b1a3f1d2-f5df-4f29-852e-906b3d8341fc
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Parallel Diagnostic Tools (Concurrency Runtime)
[!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] provides extensive support for debugging and profiling multi-threaded applications.  
  
## Debugging  
 The Visual Studio debugger includes the **Parallel Stacks** window, **Parallel Tasks** window, and **Parallel Watch** window. For more information, see [Walkthrough: Debugging a Parallel Application](../vs140/Walkthrough--Debugging-a-Parallel-Application.md) and [How to: Use the Parallel Watch Window](../vs140/How-to--Use-the-Parallel-Watch-Window.md).  
  
## Profiling  
 The profiling tools provide three data views that display graphical, tabular and numerical information about how a multi-threaded application interacts with itself and with other programs. The views enable you to quickly identify areas of concern, and to navigate from points on the graphical displays to call stacks, call sites, and source code. For more information, see [Concurrency Visualizer](../vs140/Concurrency-Visualizer.md).  
  
## Event Tracing  
 The Concurrency Runtime uses [Event Tracing for Windows](http://msdn.microsoft.com/library/windows/desktop/bb968803) (ETW) to notify instrumentation tools, such as profilers, when various events occur. These events include when a scheduler is activated or deactivated, when a context begins, ends, blocks, unblocks, or yields, and when a parallel algorithm begins or ends.  
  
 Tools such as the [Concurrency Visualizer](../vs140/Concurrency-Visualizer.md) utilize this functionality; therefore, you typically do not have to work with these events directly. However, these events are useful when you are developing a custom profiler or when you use event tracing tools such as [Xperf](http://go.microsoft.com/fwlink/?LinkID=160628).  
  
 The Concurrency Runtime raises these events only when tracing is enabled. Call the [concurrency::EnableTracing](../vs140/EnableTracing-Function.md) function to enable event tracing and the [concurrency::DisableTracing](../vs140/DisableTracing-Function.md) function to disable tracing.  
  
 The following table describes the events that the runtime raises when event tracing is enabled:  
  
|Event|Description|Value|  
|-----------|-----------------|-----------|  
|[concurrency::ConcRT_ProviderGuid](../vs140/ConcRT_ProviderGuid-Constant.md)|The ETW provider identifier for the Concurrency Runtime.|`f7b697a3-4db5-4d3b-be71-c4d284e6592f`|  
|[concurrency::ContextEventGuid](../vs140/ContextEventGuid-Constant.md)|Marks events that are related to contexts.|`5727a00f-50be-4519-8256-f7699871fecb`|  
|[concurrency::PPLParallelForEventGuid](../vs140/PPLParallelForEventGuid-Constant.md)|Marks the entrance and exit to calls to the [concurrency::parallel_for](../vs140/parallel_for-Function.md) algorithm.|`31c8da6b-6165-4042-8b92-949e315f4d84`|  
|[concurrency::PPLParallelForeachEventGuid](../vs140/PPLParallelForeachEventGuid-Constant.md)|Marks the entrance and exit to calls to the [concurrency::parallel_for_each](../vs140/parallel_for_each-Function.md) algorithm.|`5cb7d785-9d66-465d-bae1-4611061b5434`|  
|[concurrency::PPLParallelInvokeEventGuid](../vs140/PPLParallelInvokeEventGuid-Constant.md)|Marks the entrance and exit to calls to the [concurrency::parallel_invoke](../vs140/parallel_invoke-Function.md) algorithm.|`d1b5b133-ec3d-49f4-98a3-464d1a9e4682`|  
|[concurrency::SchedulerEventGuid](../vs140/SchedulerEventGuid-Constant.md)|Marks events that are related to the [Task Scheduler](../vs140/Task-Scheduler--Concurrency-Runtime-.md).|`e2091f8a-1e0a-4731-84a2-0dd57c8a5261`|  
|[concurrency::VirtualProcessorEventGuid](../vs140/VirtualProcessorEventGuid-Constant.md)|Marks events that are related to virtual processors.|`2f27805f-1676-4ecc-96fa-7eb09d44302f`|  
  
 The Concurrency Runtime defines, but does not currently raise, the following events. The runtime reserves these events for future use:  
  
-   [concurrency::ConcRTEventGuid](../vs140/ConcRTEventGuid-Constant.md)  
  
-   [concurrency::ScheduleGroupEventGuid](../vs140/SchedulerEventGuid-Constant.md)  
  
-   [concurrency::ChoreEventGuid](../vs140/ChoreEventGuid-Constant.md)  
  
-   [concurrency::LockEventGuid](../vs140/LockEventGuid-Constant.md)  
  
-   [concurrency::ResourceManagerEventGuid](../vs140/ResourceManagerEventGuid-Constant.md)  
  
 The [concurrency::ConcRT_EventType](../vs140/ConcRT_EventType-Enumeration.md) enumeration specifies the possible operations that an event tracks. For example, at the entrance of the `parallel_for` algorithm, the runtime raises the `PPLParallelForEventGuid` event and provides `CONCRT_EVENT_START` as the operation. Before the `parallel_for` algorithm returns, the runtime again raises the `PPLParallelForEventGuid` event and provides `CONCRT_EVENT_END` as the operation.  
  
 The following example illustrates how to enable tracing for a call to `parallel_for`. The runtime does not trace the first call to `parallel_for` because tracing it not enabled. The call to `EnableTracing` enables the runtime to trace the second call to `parallel_for`.  
  
 [!CODE [concrt-etw#1](../CodeSnippet/VS_Snippets_ConcRT/concrt-etw#1)]  
  
 The runtime tracks the number of times that you call `EnableTracing` and `DisableTracing`. Therefore, if you call `EnableTracing` multiple times, you must call `DisableTracing` the same number of times in order to disable tracing.  
  
## See Also  
 [Concurrency Runtime](../vs140/Concurrency-Runtime.md)