---
title: "Creating a Breakpoint"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 6f9f87bb-192e-45e0-9a7a-ffe729e87f7d
caps.latest.revision: 10
translation.priority.mt: 
  - de-de
  - ja-jp
---
# Creating a Breakpoint
The following describes the process of creating a breakpoint.  
  
## Methods in Breakpoint Creation  
 When the module that is needed to bind a breakpoint is loaded, the session debug manager (SDM) calls the following methods:  
  
1.  [IDebugPendingBreakpoint2::Enable](../vs140/IDebugPendingBreakpoint2--Enable.md)  
  
2.  [IDebugPendingBreakpoint2::Virtualize](../vs140/IDebugPendingBreakpoint2--Virtualize.md)  
  
3.  [IDebugPendingBreakpoint2::CanBind](../vs140/IDebugPendingBreakpoint2--CanBind.md)  
  
    > [!NOTE]
    >  **CanBind** is called only when a user makes a breakpoint from the Breakpoints window.  
  
4.  [IDebugPendingBreakpoint2::Bind](../vs140/IDebugPendingBreakpoint2--Bind.md)  
  
5.  [IDebugPendingBreakpoint2::EnumBoundBreakpoints](../vs140/IDebugPendingBreakpoint2--EnumBoundBreakpoints.md)  
  
## See Also  
 [Calling Debugger Events](../vs140/Calling-Debugger-Events.md)