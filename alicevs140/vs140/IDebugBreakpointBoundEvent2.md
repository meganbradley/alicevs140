---
title: "IDebugBreakpointBoundEvent2"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 24ba362e-5be1-481a-b071-e1ebd3cae6e8
caps.latest.revision: 13
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugBreakpointBoundEvent2
This interface tells the session debug manager (SDM) that a pending breakpoint has been successfully bound to a loaded program.  
  
## Syntax  
  
```  
IDebugBreakpointBoundEvent2 : IUnknown  
```  
  
## Notes for Implementers  
 The DE implements this interface as part of its support for breakpoints. The [IDebugEvent2](../vs140/IDebugEvent2.md) interface must be implemented on the same object as this interface (the SDM uses [QueryInterface](../vs140/QueryInterface.md) to access the `IDebugEvent2` interface).  
  
## Notes for Callers  
 The DE creates and sends this event object when a pending breakpoint is successfully bound to the program being debugged. The event is sent by using the [IDebugEventCallback2](../Topic/IDebugEventCallback2.md) callback function supplied by the SDM when it attached to the program being debugged.  
  
## Methods in Vtable Order  
 The following table shows the methods of `IDebugBreakpointBoundEvent2`.  
  
|Method|Description|  
|------------|-----------------|  
|[GetPendingBreakpoint](../vs140/IDebugBreakpointBoundEvent2--GetPendingBreakpoint.md)|Gets the pending breakpoint that is being bound.|  
|[EnumBoundBreakpoints](../vs140/IDebugBreakpointBoundEvent2--EnumBoundBreakpoints.md)|Creates an enumerator of breakpoints that were bound on this event.|  
  
## Remarks  
 Whenever a breakpoint is bound, an event is sent to the SDM. If the breakpoint cannot be bound, an [IDebugBreakpointErrorEvent2](../vs140/IDebugBreakpointErrorEvent2.md) is sent; otherwise, an `IDebugBreakpointBoundEvent2` is sent.  
  
## Requirements  
 Header: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [IDebugEvent2](../vs140/IDebugEvent2.md)   
 [IDebugPendingBreakpoint2](../vs140/IDebugPendingBreakpoint2.md)   
 [IDebugEventCallback2](../Topic/IDebugEventCallback2.md)   
 [IDebugBreakpointErrorEvent2](../vs140/IDebugBreakpointErrorEvent2.md)