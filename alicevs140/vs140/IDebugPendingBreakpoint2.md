---
title: "IDebugPendingBreakpoint2"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: d416b095-917e-475e-b796-ec0a03ffb8da
caps.latest.revision: 15
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugPendingBreakpoint2
This interface represents a breakpoint that is ready to bind to a code location.  
  
## Syntax  
  
```  
IDebugPendingBreakpoint2 : IUnknown  
```  
  
## Notes for Implementers  
 The debug engine (DE) implements this interface as part of its support for breakpoints.  
  
## Notes for Callers  
 A call to [CreatePendingBreakpoint](../vs140/IDebugEngine2--CreatePendingBreakpoint.md) creates a pending breakpoint from an [IDebugBreakpointRequest2](../vs140/IDebugBreakpointRequest2.md) interface. A call to [IDebugPendingBreakpoint2::Bind](../vs140/IDebugPendingBreakpoint2--Bind.md) creates an `IDebugBreakpoint2` interface that represents a bound breakpoint in the program.  
  
## Methods in Vtable Order  
 The following table shows the methods of `IDebugPendingBreakpoint2`.  
  
|Method|Description|  
|------------|-----------------|  
|[CanBind](../vs140/IDebugPendingBreakpoint2--CanBind.md)|Determines whether this pending breakpoint can bind to a code location.|  
|[Bind](../vs140/IDebugPendingBreakpoint2--Bind.md)|Binds this pending breakpoint to one or more code locations.|  
|[GetState](../vs140/IDebugPendingBreakpoint2--GetState.md)|Gets the state of this pending breakpoint.|  
|[GetBreakpointRequest](../vs140/IDebugPendingBreakpoint2--GetBreakpointRequest.md)|Gets the breakpoint request that was used to create this pending breakpoint.|  
|[Virtualize](../vs140/IDebugPendingBreakpoint2--Virtualize.md)|Toggles the virtualized state of this pending breakpoint.|  
|[Enable](../vs140/IDebugPendingBreakpoint2--Enable.md)|Toggles the enabled state of this pending breakpoint.|  
|[SetCondition](../vs140/IDebugPendingBreakpoint2--SetCondition.md)|Sets or changes the condition associated with this pending breakpoint.|  
|[SetPassCount](../vs140/IDebugPendingBreakpoint2--SetPassCount.md)|Sets or changes the pass count associated with this pending breakpoint.|  
|[EnumBoundBreakpoints](../vs140/IDebugPendingBreakpoint2--EnumBoundBreakpoints.md)|Enumerates all breakpoints bound from this pending breakpoint.|  
|[EnumErrorBreakpoints](../vs140/IDebugPendingBreakpoint2--EnumErrorBreakpoints.md)|Enumerates all error breakpoints that resulted from this pending breakpoint.|  
|[Delete](../vs140/IDebugPendingBreakpoint2--Delete.md)|Deletes this pending breakpoint and all breakpoints bound from it.|  
  
## Remarks  
 `IDebugPendingBreakpoint2` can be thought of as a provider of all the necessary information needed to bind a breakpoint to code that can be applied to one or many programs.  
  
 A pending breakpoint can potentially produce more than one bound breakpoint. For example, a breakpoint in a C++-style template could produce a bound breakpoint for each unique instance of that template.  
  
## Requirements  
 Header: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [CreatePendingBreakpoint](../vs140/IDebugEngine2--CreatePendingBreakpoint.md)   
 [GetPendingBreakpoint](../vs140/IDebugBreakpointBoundEvent2--GetPendingBreakpoint.md)   
 [GetPendingBreakpoint](../vs140/IDebugBoundBreakpoint2--GetPendingBreakpoint.md)   
 [GetPendingBreakpoint](../vs140/IDebugErrorBreakpoint2--GetPendingBreakpoint.md)