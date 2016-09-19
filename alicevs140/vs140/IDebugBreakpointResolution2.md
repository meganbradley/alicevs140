---
title: "IDebugBreakpointResolution2"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 451d5bce-b9c1-48ff-beaa-2b4c3e1ceea0
caps.latest.revision: 13
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugBreakpointResolution2
This interface represents the information that describes a bound breakpoint.  
  
## Syntax  
  
```  
IDebugBreakpointResolution2 : IUnknown  
```  
  
## Notes for Implementers  
 The debug engine (DE) implements this interface as part of its support for breakpoints. This interface provides a description of a bound breakpoint that the session debug manager uses when a user views a breakpoint's properties.  
  
## Notes for Callers  
 A call to [IDebugBoundBreakpoint2::GetBreakpointResolution](../vs140/IDebugBoundBreakpoint2--GetBreakpointResolution.md) returns this interface.  
  
## Methods in Vtable Order  
 The following table shows the methods of `IDebugBreakpointResolution2`.  
  
|Method|Description|  
|------------|-----------------|  
|[GetBreakpointType](../vs140/IDebugBreakpointResolution2--GetBreakpointType.md)|Gets the type of the breakpoint represented by this resolution.|  
|[GetResolutionInfo](../vs140/IDebugBreakpointResolution2--GetResolutionInfo.md)|Gets the breakpoint resolution information that describes this breakpoint.|  
  
## Requirements  
 Header: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [GetBreakpointResolution](../vs140/IDebugBoundBreakpoint2--GetBreakpointResolution.md)