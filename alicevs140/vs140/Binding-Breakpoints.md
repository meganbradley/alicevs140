---
title: "Binding Breakpoints"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 70737387-c52f-4dae-8865-77d4b203bf25
caps.latest.revision: 14
translation.priority.mt: 
  - de-de
  - ja-jp
---
# Binding Breakpoints
If the user sets a breakpoint, perhaps by pressing F9, the IDE formulates the request and prompts the debug session to create the breakpoint.  
  
## Setting a Breakpoint  
 Setting a breakpoint is a two-step process, because the code or data affected by the breakpoint might not yet be available. First, the breakpoint must be described, and then, as code or data becomes available, it must be bound to that code or data, as follows:  
  
1.  The breakpoint is requested from the relevant debug engines (DEs), and then the breakpoint is bound to the code or data as it becomes available.  
  
2.  The breakpoint request is sent to the debug session, which sends it to all relevant DEs. Any DE that chooses to handle the breakpoint creates a corresponding pending breakpoint.  
  
3.  The debug session collects the pending breakpoints and sends them back to the debug package (the debugging component of Visual Studio).  
  
4.  The debug package prompts the debug session to bind the pending breakpoint to code or data. The debug session sends this request to all relevant DEs.  
  
5.  If the DE is able to bind the breakpoint, it sends a breakpoint bound event back to the debug session. If not, it sends a breakpoint error event instead.  
  
## Pending Breakpoints  
 A pending breakpoint can bind to multiple code locations. For example, a line of source code for a C++ template can bind to every code sequence generated from the template. The debug session can use a breakpoint bound event to enumerate the code contexts bound to a breakpoint at the time the event was sent. More code contexts can be bound later, so the DE may send multiple breakpoint bound events for each bind request. However, a DE should send only one breakpoint error event per bind request.  
  
## Implementation  
 Programmatically, the debug package calls the session debug manager (SDM) and gives it an [IDebugBreakpointRequest2](../vs140/IDebugBreakpointRequest2.md) interface that wraps a [BP_REQUEST_INFO](../vs140/BP_REQUEST_INFO.md) structure, which describes the breakpoint to be set. Although breakpoints can be of many forms, they ultimately resolve to a code or data context.  
  
 The SDM passes this call to each relevant DE by calling its [CreatePendingBreakpoint](../vs140/IDebugEngine2--CreatePendingBreakpoint.md) method. If the DE chooses to handle the breakpoint, it creates and returns an [IDebugPendingBreakpoint2](../vs140/IDebugPendingBreakpoint2.md) interface. The SDM collects these interfaces and passes them back to the debug package as a single `IDebugPendingBreakpoint2` interface.  
  
 So far, no events have been generated.  
  
 The debug package then attempts to bind the pending breakpoint to code or data by calling [Bind](../vs140/IDebugPendingBreakpoint2--Bind.md), which is implemented by the DE.  
  
 If the breakpoint is bound, the DE sends an [IDebugBreakpointBoundEvent2](../vs140/IDebugBreakpointBoundEvent2.md) event interface to the debug package. The debug package uses this interface to enumerate all code contexts (or the single data context) bound to the breakpoint by calling [EnumBoundBreakpoints](../vs140/IDebugBreakpointBoundEvent2--EnumBoundBreakpoints.md), which returns one or more [IDebugBoundBreakpoint2](../vs140/IDebugBoundBreakpoint2.md) interfaces. The [GetBreakpointResolution](../vs140/IDebugBoundBreakpoint2--GetBreakpointResolution.md) interface returns an [IDebugBreakpointResolution2](../vs140/IDebugBreakpointResolution2.md) interface, and [GetResolutionInfo](../vs140/IDebugBreakpointResolution2--GetResolutionInfo.md) returns a [BP_RESOLUTION_INFO](../vs140/BP_RESOLUTION_INFO.md) union containing the code or data context.  
  
 If the DE is unable to bind the breakpoint, it sends a single [IDebugBreakpointErrorEvent2](../vs140/IDebugBreakpointErrorEvent2.md) event interface to the debug package. The debug package retrieves the error type (error or warning) and informational message by calling [GetErrorBreakpoint](../vs140/IDebugBreakpointErrorEvent2--GetErrorBreakpoint.md), followed by [GetBreakpointResolution](../vs140/IDebugErrorBreakpoint2--GetBreakpointResolution.md) and [GetResolutionInfo](../vs140/IDebugErrorBreakpointResolution2--GetResolutionInfo.md). This returns a [BP_ERROR_RESOLUTION_INFO](../vs140/BP_ERROR_RESOLUTION_INFO.md) structure that contains the error type and message.  
  
 If a DE handles a breakpoint but cannot bind it, it returns an error of type `BPET_TYPE_ERROR`. The debug package responds by displaying an error dialog box, and the IDE places an exclamation glyph inside the breakpoint glyph to the left of the source code line.  
  
 If a DE handles a breakpoint, cannot bind it, but some other DE might bind it, it returns a warning. The IDE responds by placing a question glyph inside the breakpoint glyph to the left of the source code line.  
  
## See Also  
 [Debugging Tasks](../vs140/Debugging-Tasks.md)