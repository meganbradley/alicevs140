---
title: "IEnumDebugBoundBreakpoints2"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: ea03e7e1-28d6-40b7-8097-bbb61d3b7caa
caps.latest.revision: 13
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IEnumDebugBoundBreakpoints2
This interface enumerates the bound breakpoints associated with a pending breakpoint or breakpoint bound event.  
  
## Syntax  
  
```  
IEnumDebugBoundBreakpoints2 : IUnknown  
```  
  
## Notes for Implementers  
 The debug engine (DE) implements this interface as part of its support for breakpoints. This interface must be implemented if breakpoints are supported.  
  
## Notes for Callers  
 Visual Studio calls:  
  
-   [IDebugBreakpointEvent2::EnumBreakpoints](../vs140/IDebugBreakpointEvent2--EnumBreakpoints.md) to obtain this interface representing a list of all breakpoints that were triggered.  
  
-   [IDebugBreakpointBoundEvent2::EnumBoundBreakpoints](../vs140/IDebugBreakpointBoundEvent2--EnumBoundBreakpoints.md) to obtain this interface representing a list of all breakpoints that were bound.  
  
-   [IDebugPendingBreakpoint2::EnumBoundBreakpoints](../vs140/IDebugPendingBreakpoint2--EnumBoundBreakpoints.md) to obtain this interface representing a list of all breakpoints bound to that pending breakpoint.  
  
## Methods in Vtable Order  
 The following table shows the methods of `IEnumDebugBoundBreakpoints2`.  
  
|Method|Description|  
|------------|-----------------|  
|[Next](../vs140/IEnumDebugBoundBreakpoints2--Next.md)|Retrieves a specified number of bound breakpoints in an enumeration sequence.|  
|[Skip](../vs140/IEnumDebugBoundBreakpoints2--Skip.md)|Skips a specified number of bound breakpoints in an enumeration sequence.|  
|[Reset](../vs140/IEnumDebugBoundBreakpoints2--Reset.md)|Resets an enumeration sequence to the beginning.|  
|[Clone](../vs140/IEnumDebugBoundBreakpoints2--Clone.md)|Creates an enumerator that contains the same enumeration state as the current enumerator.|  
|[GetCount](../vs140/IEnumDebugBoundBreakpoints2--GetCount.md)|Gets the number of bound breakpoints in an enumerator.|  
  
## Remarks  
 Visual Studio uses the bound breakpoints represented by this interface to update the display of breakpoints in the IDE.  
  
## Requirements  
 Header: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [Core Interfaces](../vs140/Core-Interfaces.md)   
 [EnumBoundBreakpoints](../vs140/IDebugBreakpointBoundEvent2--EnumBoundBreakpoints.md)   
 [EnumBoundBreakpoints](../vs140/IDebugPendingBreakpoint2--EnumBoundBreakpoints.md)   
 [IDebugPendingBreakpoint2::EnumBoundBreakpoints](../vs140/IDebugPendingBreakpoint2--EnumBoundBreakpoints.md)