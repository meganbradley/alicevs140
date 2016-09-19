---
title: "IDebugErrorBreakpointResolution2"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: b1234216-0ac8-461d-b2a7-54f60f8f3262
caps.latest.revision: 13
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugErrorBreakpointResolution2
This interface represents the resolution of a breakpoint error.  
  
## Syntax  
  
```  
IDebugErrorBreakpointResolution2 : IUnknown  
```  
  
## Notes for Implementers  
 A debug engine implements this interface as part of its support for breakpoints. This interface is used to report where a breakpoint failed to bind.  
  
## Notes for Callers  
 A call to [IDebugErrorBreakpoint2::GetBreakpointResolution](../vs140/IDebugErrorBreakpoint2--GetBreakpointResolution.md) returns this interface to provide information about where the breakpoint failed to bind. The [IDebugBreakpointErrorEvent2::GetErrorBreakpoint](../vs140/IDebugBreakpointErrorEvent2--GetErrorBreakpoint.md) method obtains the [IDebugErrorBreakpoint2](../vs140/IDebugErrorBreakpoint2.md) interface.  
  
## Methods in Vtable Order  
 The following table shows the methods of `IDebugErrorBreakpointResolution2`.  
  
|Method|Description|  
|------------|-----------------|  
|[GetBreakpointType](../vs140/IDebugErrorBreakpointResolution2--GetBreakpointType.md)|Gets the breakpoint type.|  
|[GetResolutionInfo](../vs140/IDebugErrorBreakpointResolution2--GetResolutionInfo.md)|Gets the breakpoint resolution information.|  
  
## Requirements  
 Header: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [IDebugErrorBreakpoint2](../vs140/IDebugErrorBreakpoint2.md)   
 [GetBreakpointResolution](../vs140/IDebugErrorBreakpoint2--GetBreakpointResolution.md)   
 [IDebugBreakpointErrorEvent2::GetErrorBreakpoint](../vs140/IDebugBreakpointErrorEvent2--GetErrorBreakpoint.md)