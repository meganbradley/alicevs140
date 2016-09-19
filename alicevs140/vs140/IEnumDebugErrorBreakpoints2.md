---
title: "IEnumDebugErrorBreakpoints2"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: ffdad73d-969a-45ef-9ad1-7f5d3b814018
caps.latest.revision: 11
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IEnumDebugErrorBreakpoints2
This interface enumerates the error breakpoints associated with a pending breakpoint.  
  
## Syntax  
  
```  
IEnumDebugErrorBreakpoints2 : IUnknown  
```  
  
## Notes for Implementers  
 The debug engine (DE) implements this interface as part of its support for breakpoints.  
  
## Notes for Callers  
 Visual Studio calls [IDebugPendingBreakpoint2::CanBind](../vs140/IDebugPendingBreakpoint2--CanBind.md) to obtain this interface representing a list of breakpoints that cannot be bound, or [IDebugPendingBreakpoint2::EnumErrorBreakpoints](../vs140/IDebugPendingBreakpoint2--EnumErrorBreakpoints.md) to obtain this interface representing a list of breakpoints that were not bound.  
  
## Methods in Vtable Order  
 The following table shows the methods of `IEnumDebugErrorBreakpoints2`.  
  
|Method|Description|  
|------------|-----------------|  
|[Next](../vs140/IEnumDebugErrorBreakpoints2--Next.md)|Retrieves a specified number of error breakpoints in an enumeration sequence.|  
|[Skip](../vs140/IEnumDebugErrorBreakpoints2--Skip.md)|Skips a specified number of error breakpoints in an enumeration sequence.|  
|[Reset](../vs140/IEnumDebugErrorBreakpoints2--Reset.md)|Resets an enumeration sequence to the beginning.|  
|[Clone](../vs140/IEnumDebugErrorBreakpoints2--Clone.md)|Creates an enumerator that contains the same enumeration state as the current enumerator.|  
|[GetCount](../vs140/IEnumDebugErrorBreakpoints2--GetCount.md)|Gets the number of error breakpoints in an enumerator.|  
  
## Remarks  
 This interface holds a list of [IDebugErrorBreakpoint2](../vs140/IDebugErrorBreakpoint2.md) interfaces, each of which describes a breakpoint that could not be bound and why it could not be bound. Visual Studio uses the `IEnumDebugErrorBreakpoint2` interface to update the breakpoints shown in the IDE.  
  
## Requirements  
 Header: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [Core Interfaces](../vs140/Core-Interfaces.md)   
 [CanBind](../vs140/IDebugPendingBreakpoint2--CanBind.md)   
 [EnumErrorBreakpoints](../vs140/IDebugPendingBreakpoint2--EnumErrorBreakpoints.md)   
 [IDebugErrorBreakpoint2](../vs140/IDebugErrorBreakpoint2.md)