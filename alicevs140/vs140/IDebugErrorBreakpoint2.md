---
title: "IDebugErrorBreakpoint2"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 1f2a4b94-3713-46e9-8272-3917187792bd
caps.latest.revision: 13
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugErrorBreakpoint2
This interface represents an error or warning breakpoint, such as an invalid location, an invalid expression, or the reasons why the pending breakpoint has not bound (code not loaded yet, and so on).  
  
## Syntax  
  
```  
IDebugErrorBreakpoint2 : IUnknown  
```  
  
## Notes for Implementers  
 A debug engine implements this interface as part of its support for breakpoints. This interface is used to report problems with binding a breakpoint.  
  
## Notes for Callers  
 A call to [IDebugBreakpointErrorEvent2::GetErrorBreakpoint](../vs140/IDebugBreakpointErrorEvent2--GetErrorBreakpoint.md) obtains this interface. This interface can also be returned (as part of a list represented by an [IEnumDebugErrorBreakpoints2](../vs140/IEnumDebugErrorBreakpoints2.md) interface) by a call to [IDebugPendingBreakpoint2::CanBind](../vs140/IDebugPendingBreakpoint2--CanBind.md) or [IDebugPendingBreakpoint2::EnumErrorBreakpoints](../vs140/IDebugPendingBreakpoint2--EnumErrorBreakpoints.md).  
  
## Methods in Vtable Order  
 The following table shows the methods of `IDebugErrorBreakpoint2`.  
  
|Method|Description|  
|------------|-----------------|  
|[GetPendingBreakpoint](../vs140/IDebugErrorBreakpoint2--GetPendingBreakpoint.md)|Gets the pending breakpoint that caused the error.|  
|[GetBreakpointResolution](../vs140/IDebugErrorBreakpoint2--GetBreakpointResolution.md)|Gets the breakpoint error resolution that describes the error.|  
  
## Requirements  
 Header: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [IDebugBreakpointErrorEvent2](../vs140/IDebugBreakpointErrorEvent2.md)   
 [GetErrorBreakpoint](../vs140/IDebugBreakpointErrorEvent2--GetErrorBreakpoint.md)   
 [IEnumDebugErrorBreakpoints2](../vs140/IEnumDebugErrorBreakpoints2.md)   
 [Next](../vs140/IEnumDebugErrorBreakpoints2--Next.md)   
 [IDebugPendingBreakpoint2](../vs140/IDebugPendingBreakpoint2.md)   
 [IDebugErrorBreakpointResolution2](../vs140/IDebugErrorBreakpointResolution2.md)