---
title: "IDebugBreakpointRequest2"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 01ac4013-96f9-4235-b289-f55f9e99558f
caps.latest.revision: 16
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugBreakpointRequest2
This interface represents the information necessary to create and bind any type of breakpoint.  
  
## Syntax  
  
```  
IDebugBreakpointRequest2 : IUnknown  
```  
  
## Notes for Implementers  
 The session debug manager (SDM) typically implements this interface.  
  
## Notes for Callers  
 The debug engine (DE) receives this interface through a call to [IDebugEngine2::CreatePendingBreakpoint](../vs140/IDebugEngine2--CreatePendingBreakpoint.md) in order to create a pending breakpoint. A call to [IDebugPendingBreakpoint2::GetBreakpointRequest](../vs140/IDebugPendingBreakpoint2--GetBreakpointRequest.md) can retrieve this interface from the DE.  
  
## Methods in Vtable Order  
 The following table shows the methods of `IDebugBreakpointRequest2`.  
  
|Method|Description|  
|------------|-----------------|  
|[IDebugBreakpointRequest2::GetLocationType](../vs140/IDebugBreakpointRequest2--GetLocationType.md)|Gets the breakpoint location type of this breakpoint request.|  
|[IDebugBreakpointRequest2::GetRequestInfo](../vs140/IDebugBreakpointRequest2--GetRequestInfo.md)|Gets the breakpoint request information that describes this breakpoint request.|  
  
## Remarks  
 After the program being debugged has been loaded, a call to [IDebugPendingBreakpoint2::Bind](../vs140/IDebugPendingBreakpoint2--Bind.md) binds a pending breakpoint to the requested location in the program.  
  
## Requirements  
 Header: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [CreatePendingBreakpoint](../vs140/IDebugEngine2--CreatePendingBreakpoint.md)   
 [GetBreakpointRequest](../vs140/IDebugPendingBreakpoint2--GetBreakpointRequest.md)   
 [IDebugPendingBreakpoint2::Bind](../vs140/IDebugPendingBreakpoint2--Bind.md)