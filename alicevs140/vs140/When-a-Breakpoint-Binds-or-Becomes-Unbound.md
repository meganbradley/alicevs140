---
title: "When a Breakpoint Binds or Becomes Unbound"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 61bf00b2-8293-49d3-b919-1efb0dec9151
caps.latest.revision: 9
translation.priority.mt: 
  - de-de
  - ja-jp
---
# When a Breakpoint Binds or Becomes Unbound
When a breakpoint cannot be bound at the time a call is made to the [IDebugPendingBreakpoint2::CanBind](../vs140/IDebugPendingBreakpoint2--CanBind.md) method, the bind time and create time of the breakpoint are different.  
  
## Methods Called  
 The session debug manager (SDM) calls the following methods:  
  
1.  [IDebugEngine2::CreatePendingBreakpoint](../vs140/IDebugEngine2--CreatePendingBreakpoint.md). The DE returns an [IDebugPendingBreakpoint2](../vs140/IDebugPendingBreakpoint2.md).  
  
2.  [IDebugPendingBreakpoint2::Enable](../vs140/IDebugPendingBreakpoint2--Enable.md).  
  
3.  [IDebugPendingBreakpoint2::Virtualize](../vs140/IDebugPendingBreakpoint2--Virtualize.md).  
  
4.  The [IDebugPendingBreakpoint2::Bind](../vs140/IDebugPendingBreakpoint2--Bind.md) method and returns S_OK. The DE sends an [IDebugBreakpointBoundEvent2](../vs140/IDebugBreakpointBoundEvent2.md) or [IDebugBreakpointErrorEvent2](../vs140/IDebugBreakpointErrorEvent2.md).  
  
5.  [IDebugBreakpointBoundEvent2::GetPendingBreakpoint](../vs140/IDebugBreakpointBoundEvent2--GetPendingBreakpoint.md) and [IDebugBreakpointBoundEvent2::EnumBoundBreakpoints](../vs140/IDebugBreakpointBoundEvent2--EnumBoundBreakpoints.md) methods to verify and to get the bound breakpoints.  
  
## See Also  
 [Calling Debugger Events](../vs140/Calling-Debugger-Events.md)