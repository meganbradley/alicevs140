---
title: "Breakpoint Errors"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 79221c6b-a924-4c8e-a778-e312e4e0c0c8
caps.latest.revision: 10
translation.priority.mt: 
  - de-de
  - ja-jp
---
# Breakpoint Errors
The following describes the process when a breakpoint attempts to bind to code but fails:  
  
## Troubleshooting a Breakpoint Error  
  
1.  The debug engine (DE) sends an [IDebugBreakpointErrorEvent2](../vs140/IDebugBreakpointErrorEvent2.md) to the session debug manager (SDM).  
  
2.  The SDM calls [IDebugBreakpointErrorEvent2::GetErrorBreakpoint](../vs140/IDebugBreakpointErrorEvent2--GetErrorBreakpoint.md) (IDebugErrorBreakpoint2** `ppErrorBP`) to get the error breakpoint.  
  
3.  The SDM calls [IDebugErrorBreakpoint2::GetPendingBreakpoint](../vs140/IDebugErrorBreakpoint2--GetPendingBreakpoint.md) to get the pending breakpoint from which the error breakpoint originated.  
  
4.  The SDM calls [IDebugErrorBreakpoint2::GetBreakpointResolution](../vs140/IDebugErrorBreakpoint2--GetBreakpointResolution.md) to get the reason why the error breakpoint failed to bind.  
  
## See Also  
 [Calling Debugger Events](../vs140/Calling-Debugger-Events.md)