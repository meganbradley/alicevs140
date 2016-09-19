---
title: "IDebugBreakpointRequest3"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 8a042beb-b319-48e3-b3c8-9c8336ab371b
caps.latest.revision: 10
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugBreakpointRequest3
This interface represents the information necessary to create and bind any type of breakpoint. It is an extension of [IDebugBreakpointRequest2](../vs140/IDebugBreakpointRequest2.md).  
  
## Syntax  
  
```  
IDebugBreakpointRequest3 : IDebugBreakpointRequest2  
```  
  
## Notes for Implementers  
 The session debug manager (SDM) typically implements this interface.  
  
## Notes for Callers  
 The debug engine (DE) accesses this interface by calling [QueryInterface](../vs140/QueryInterface.md) on the IDebugBreakpointRequest2 interface received in a call to [IDebugEngine2::CreatePendingBreakpoint](../vs140/IDebugEngine2--CreatePendingBreakpoint.md).  
  
## Methods in Vtable Order  
 In addition to the methods inherited from [IDebugBreakpointRequest2](../vs140/IDebugBreakpointRequest2.md), the `IDebugBreakpointRequest3` interface exposes the following method.  
  
|Method|Description|  
|------------|-----------------|  
|[GetRequestInfo2](../vs140/IDebugBreakpointRequest3--GetRequestInfo2.md)|Gets the breakpoint request information that describes this breakpoint request.|  
  
## Remarks  
 This interface is used to provide additional information to the DE through the [BP_REQUEST_INFO2](../vs140/BP_REQUEST_INFO2.md) structure. This additional information includes the DE's vendor ID (in the form of a GUID), the name of a tracepoint, and the name of a breakpoint constraint.  
  
## Requirements  
 Header: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [IDebugBreakpointRequest2](../vs140/IDebugBreakpointRequest2.md)   
 [BP_REQUEST_INFO2](../vs140/BP_REQUEST_INFO2.md)