---
title: "Program Control"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 6be80904-e66c-4cae-8891-1113b799fb01
caps.latest.revision: 11
translation.priority.mt: 
  - de-de
  - ja-jp
---
# Program Control
In Visual Studio debugging, all of the following stepping and continuing routines occur at the program level:  
  
-   Setting the next statement, that is, setting your computer to the next instruction to be executed in a particular frame environment  
  
-   Executing, that is, continuing to exit out of stepping mode  
  
-   Stepping to the next instruction  
  
-   Continuing with the current stepping mode  
  
-   Suspending the threads contained by the program  
  
-   Resuming the threads contained by the program  
  
> [!NOTE]
>  Viewing the call stack is implemented on the thread level. To enumerate the frame information when viewing the call stack for a thread, you must implement all the methods of the [IEnumDebugFrameInfo2](../vs140/IEnumDebugFrameInfo2.md) interface.  
  
## Methods of Program Control  
 The following table shows the methods of [IDebugProgram2](../vs140/IDebugProgram2.md) that must be implemented for a minimally functional debug engine (DE) and execution control.  
  
|Method|Description|  
|------------|-----------------|  
|[IDebugProgram2::Execute](../vs140/IDebugProgram2--Execute.md)|Continues running all threads contained by a program from a stopped state. Required for execution control.|  
|[IDebugProgram2::Continue](../vs140/IDebugProgram2--Continue.md)|Continues running all threads contained by a program from a stopped state. Required for execution control.|  
|[IDebugProgram2::Step](../vs140/IDebugProgram2--Step.md)|Performs a step on the given thread. Continues running all other threads contained by the program. Required for execution control.|  
  
 For multithreaded programs, you must also implement the [IDebugProgram2::EnumThreads](../vs140/IDebugProgram2--EnumThreads.md) method and all the methods of the [IEnumDebugThreads2](../vs140/IEnumDebugThreads2.md) interface.  
  
## See Also  
 [Execution Control and State Evaluation](../vs140/Execution-Control-and-State-Evaluation.md)