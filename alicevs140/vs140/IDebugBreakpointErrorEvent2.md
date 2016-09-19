---
title: "IDebugBreakpointErrorEvent2"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: adee79df-8db5-4510-a7df-c50f4dbf5e35
caps.latest.revision: 16
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugBreakpointErrorEvent2
This interface tells the session debug manager (SDM) that a pending breakpoint could not be bound to a loaded program, either because of a warning or an error.  
  
## Syntax  
  
```  
IDebugBreakpointErrorEvent2 : IUnknown  
```  
  
## Notes for Implementers  
 The DE implements this interface as part of its support for breakpoints. The [IDebugEvent2](../vs140/IDebugEvent2.md) interface must be implemented on the same object as this interface (the SDM uses [QueryInterface](../vs140/QueryInterface.md) to access the `IDebugEvent2` interface).  
  
## Notes for Callers  
 The DE creates and sends this event object when a pending breakpoint cannot be bound to the program being debugged. The event is sent by using the [IDebugEventCallback2](../Topic/IDebugEventCallback2.md) callback function supplied by the SDM when it attached to the program being debugged.  
  
## Methods in Vtable Order  
 The following table shows the methods of `IDebugBreakpointErrorEvent2`.  
  
|Method|Description|  
|------------|-----------------|  
|[GetErrorBreakpoint](../vs140/IDebugBreakpointErrorEvent2--GetErrorBreakpoint.md)|Gets the [IDebugErrorBreakpoint2](../vs140/IDebugErrorBreakpoint2.md) interface that describes the warning or error.|  
  
## Remarks  
 Whenever a breakpoint is bound, an event is sent to the SDM. If the breakpoint cannot be bound, an `IDebugBreakpointErrorEvent2` is sent; otherwise, an [IDebugBreakpointBoundEvent2](../vs140/IDebugBreakpointBoundEvent2.md) is sent.  
  
 For example, when the condition associated with the pending breakpoint fails to parse or evaluate, a warning is sent that the pending breakpoint cannot be bound at this time. This may occur if the code for the breakpoint has not loaded yet.  
  
## Requirements  
 Header: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [IDebugEvent2](../vs140/IDebugEvent2.md)   
 [IDebugErrorBreakpoint2](../vs140/IDebugErrorBreakpoint2.md)   
 [IDebugPendingBreakpoint2](../vs140/IDebugPendingBreakpoint2.md)   
 [IDebugBreakpointBoundEvent2](../vs140/IDebugBreakpointBoundEvent2.md)   
 [IDebugEventCallback2](../Topic/IDebugEventCallback2.md)