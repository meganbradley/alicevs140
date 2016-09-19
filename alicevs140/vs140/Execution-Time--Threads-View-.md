---
title: "Execution Time (Threads View)"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-debug
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 80c100f8-2502-4613-bfef-4f4f2e09cc8d
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Execution Time (Threads View)
These segments in the Threads View timeline represent execution time, when the thread is actively doing work on a logical core in the system.  
  
 Changes in thread status are detected through kernel context switch events. Event Tracing for Windows (ETW) captures sample stacks every millisecond. In a very short green segment, it is possible that no sample is taken. Therefore, some short execution segments may show no call stack.  
  
 When you click an execution segment, the Concurrency Visualizer displays the sample stack closest to the location of the click. The location of that sample stack is shown by a black arrow, or caret, above the timeline and the sample stack appears on the **Current** tab.  
  
 To see a traditional sampling profile for all execution segments in the current view, click **Execution** in the Visible Timeline Profile.  
  
## See Also  
 [Execution Profile Report](../vs140/Execution-Profile-Report.md)   
 [Threads View (Parallel Performance)](../vs140/Threads-View--Parallel-Performance-.md)