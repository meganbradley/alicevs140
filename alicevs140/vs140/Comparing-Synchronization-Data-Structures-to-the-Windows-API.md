---
title: "Comparing Synchronization Data Structures to the Windows API"
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
ms.assetid: 8b0b1a3a-ef80-408c-91fa-93e6af920b4e
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Comparing Synchronization Data Structures to the Windows API
This topic compares the behavior of the synchronization data structures that are provided by the Concurrency Runtime to those provided by the Windows API.  
  
 The synchronization data structures that are provided by the Concurrency Runtime follow the *cooperative threading model*. In the cooperative threading model, synchronization primitives explicitly yield their processing resources to other threads. This differs from the *preemptive threading model*, where processing resources are transferred to other threads by the controlling scheduler or operating system.  
  
## critical_section  
 The [concurrency::critical_section](../vs140/critical_section-Class.md) class resembles the Windows `CRITICAL_SECTION` structure because it can be used only by the threads of one process. For more information about critical sections in the Windows API, see [Critical Section Objects](http://msdn.microsoft.com/library/windows/desktop/ms682530).  
  
## reader_writer_lock  
 The [concurrency::reader_writer_lock](../vs140/reader_writer_lock-Class.md) class resembles Windows slim reader/writer (SRW) locks. The following table explains the similarities and differences.  
  
|Feature|`reader_writer_lock`|SRW lock|  
|-------------|--------------------------|--------------|  
|Non-reentrant|Yes|Yes|  
|Can promote a reader to a writer (upgrade support)|No|No|  
|Can demote a writer to a reader (downgrade support)|No|No|  
|Write-preference lock|Yes|No|  
|FIFO access to writers|Yes|No|  
  
 For more information about SRW locks, see [Slim Reader/Writer (SRW) Locks](http://msdn.microsoft.com/library/windows/desktop/aa904937) in the Platform SDK.  
  
## event  
 The [concurrency::event](../vs140/event-Class.md) class resembles an unnamed, Windows manual-reset event. However, an `event` object behaves cooperatively, whereas a Windows event behaves preemptively. For more information about Windows events, see [Event Objects](http://msdn.microsoft.com/library/windows/desktop/ms682655).  
  
## Example  
  
### Description  
 To better understand the difference between the `event` class and Windows events, consider the following example. This example enables the scheduler to create at most two simultaneous tasks and then calls two similar functions that use the `event` class and a Windows manual-reset event. Each function first creates several tasks that wait for a shared event to become signaled. Each function then yields to the running tasks and then signals the event. Each function then waits for the signaled event.  
  
### Code  
 [!CODE [concrt-event-comparison#1](../CodeSnippet/VS_Snippets_ConcRT/concrt-event-comparison#1)]  
  
### Comments  
 This example produces the following sample output:  
  
 **Cooperative event:**  
 **Context 0: waiting on an event.**  
 **Context 1: waiting on an event.**  
 **Context 2: waiting on an event.**  
 **Context 3: waiting on an event.**  
 **Context 4: waiting on an event.**  
 **Setting the event.**  
 **Context 5: received the event.**  
 **Context 6: received the event.**  
 **Context 7: received the event.**  
 **Context 8: received the event.**  
 **Context 9: received the event.**  
**Windows event:**  
 **Context 10: waiting on an event.**  
 **Context 11: waiting on an event.**  
 **Setting the event.**  
 **Context 12: received the event.**  
 **Context 14: waiting on an event.**  
 **Context 15: received the event.**  
 **Context 16: waiting on an event.**  
 **Context 17: received the event.**  
 **Context 18: waiting on an event.**  
 **Context 19: received the event.**  
 **Context 13: received the event.** Because the `event` class behaves cooperatively, the scheduler can reallocate processing resources to another context when an event is waiting to enter the signaled state. Therefore, more work is accomplished by the version that uses the `event` class. In the version that uses Windows events, each waiting task must enter the signaled state before the next task is started.  
  
 For more information about tasks, see [Task Parallelism](../vs140/Task-Parallelism--Concurrency-Runtime-.md).  
  
## See Also  
 [Synchronization Data Structures](../vs140/Synchronization-Data-Structures.md)   
 [Critical Section Objects](http://msdn.microsoft.com/library/windows/desktop/ms682530)   
 [Slim Reader/Writer (SRW) Locks](http://msdn.microsoft.com/library/windows/desktop/aa904937)   
 [Event Objects](http://msdn.microsoft.com/library/windows/desktop/ms682655)