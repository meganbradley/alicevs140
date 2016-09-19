---
title: "IDebugBreakpointUnboundEvent2"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 6b1e1863-0c64-4d85-8ab9-aface522fdea
caps.latest.revision: 13
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugBreakpointUnboundEvent2
This interface tells the session debug manager (SDM) that a bound breakpoint has been unbound from a loaded program.  
  
## Syntax  
  
```  
IDebugBreakpointUnboundEvent2 : IUnknown  
```  
  
## Notes for Implementers  
 The debug engine (DE) implements this interface as part of its support for breakpoints. The [IDebugEvent2](../vs140/IDebugEvent2.md) interface must be implemented on the same object as this interface (the SDM uses [QueryInterface](../vs140/QueryInterface.md) to access the `IDebugEvent2` interface).  
  
## Notes for Callers  
 The DE creates and sends this event object when a bound breakpoint has been unbound. The event is sent by using the [IDebugEventCallback2](../Topic/IDebugEventCallback2.md) callback function supplied by the SDM when it attached to the program being debugged.  
  
## Methods in Vtable Order  
 The following table shows the methods of `IDebugBreakpointUnboundEvent2`.  
  
|Method|Description|  
|------------|-----------------|  
|[GetBreakpoint](../vs140/IDebugBreakpointUnboundEvent2--GetBreakpoint.md)|Gets the breakpoint that became unbound.|  
|[GetReason](../vs140/IDebugBreakpointUnboundEvent2--GetReason.md)|Gets the reason the breakpoint was unbound.|  
  
## Remarks  
 When a debug engine DLL or class unloads, all breakpoints that were bound to code in that module must be unbound from the program being debugged. An `IDebugBreakpointUnboundEvent2` is sent for each unbound breakpoint.  
  
## Requirements  
 Header: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [IDebugEvent2](../vs140/IDebugEvent2.md)   
 [IDebugBoundBreakpoint2](../vs140/IDebugBoundBreakpoint2.md)   
 [IDebugEventCallback2](../Topic/IDebugEventCallback2.md)