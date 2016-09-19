---
title: "IDebugThread2"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 221b4b1b-4a26-466e-bc29-5eff800fab13
caps.latest.revision: 14
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugThread2
This interface represents a thread running in a program.  
  
## Syntax  
  
```  
IDebugThread2 : IUnknown  
```  
  
## Notes for Implementers  
 The debug engine (DE) implements this interface to represent a thread of execution in a single program.  
  
## Notes for Callers  
 Call [IDebugStackFrame2::GetThread](../vs140/IDebugStackFrame2--GetThread.md) to obtain this interface representing the currently active thread.  
  
 This interface is also used in creating a breakpoint request (see [BP_REQUEST_INFO](../vs140/BP_REQUEST_INFO.md)).  
  
 This interface is also returned when resolving a bound or error breakpoint (see [BP_RESOLUTION_INFO](../vs140/BP_RESOLUTION_INFO.md) and [BP_ERROR_RESOLUTION_INFO](../vs140/BP_ERROR_RESOLUTION_INFO.md)).  
  
## Methods in Vtable Order  
 The following table shows the methods of `IDebugThread2`.  
  
|Method|Description|  
|------------|-----------------|  
|[EnumFrameInfo](../vs140/IDebugThread2--EnumFrameInfo.md)|Retrieves a list of the stack frames for this thread.|  
|[GetName](../vs140/IDebugThread2--GetName.md)|Gets the name of the thread.|  
|[SetThreadName](../vs140/IDebugThread2--SetThreadName.md)|Sets the name of the thread.|  
|[GetProgram](../vs140/IDebugThread2--GetProgram.md)|Gets the program in which a thread is running.|  
|[CanSetNextStatement](../vs140/IDebugThread2--CanSetNextStatement.md)|Determines whether the next statement can be set to the given stack frame and code context.|  
|[SetNextStatement](../vs140/IDebugThread2--SetNextStatement.md)|Sets the next statement to the given stack frame and code context.|  
|[GetThreadId](../vs140/IDebugThread2--GetThreadId.md)|Gets the system thread identifier.|  
|[Suspend](../vs140/IDebugThread2--Suspend.md)|Suspends a thread.|  
|[Resume](../vs140/IDebugThread2--Resume.md)|Resumes a thread.|  
|[GetThreadProperties](../vs140/IDebugThread2--GetThreadProperties.md)|Gets properties that describe a thread.|  
|[GetLogicalThread](../vs140/IDebugThread2--GetLogicalThread.md)|Gets the logical thread associated with this physical thread.|  
  
## Remarks  
 Because a single physical thread can run in multiple programs, more than one `IDebugThread2` from more than one program can represent the same physical thread.  
  
 When a breakpoint or exception occurs, an event is sent by calling [IDebugEventCallback2::Event](../vs140/IDebugEventCallback2--Event.md). One of the arguments to this method is an `IDebugThread2` interface representing the current thread. [IDebugThread2::EnumFrameInfo](../vs140/IDebugThread2--EnumFrameInfo.md) is used to obtain the [IDebugStackFrame2](../vs140/IDebugStackFrame2.md) interface for the current stack frame.  
  
## Requirements  
 Header: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [Core Interfaces](../vs140/Core-Interfaces.md)   
 [Event](../vs140/IDebugEventCallback2--Event.md)   
 [GetThread](../vs140/IDebugStackFrame2--GetThread.md)   
 [BP_REQUEST_INFO](../vs140/BP_REQUEST_INFO.md)   
 [BP_RESOLUTION_INFO](../vs140/BP_RESOLUTION_INFO.md)   
 [BP_ERROR_RESOLUTION_INFO](../vs140/BP_ERROR_RESOLUTION_INFO.md)