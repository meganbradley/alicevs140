---
title: "Deleting a Breakpoint"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 75a046cc-d20a-4c79-ad2d-1f18426ac5d0
caps.latest.revision: 9
translation.priority.mt: 
  - de-de
  - ja-jp
---
# Deleting a Breakpoint
The following describes the process when deleting a pending breakpoint:  
  
## Deletion Process  
 The session debug manager (SDM) calls the [IDebugPendingBreakpoint2::Delete](../vs140/IDebugPendingBreakpoint2--Delete.md) method to remove the pending breakpoint and all bound breakpoints bound from it.  
  
> [!NOTE]
>  A single bound breakpoint can also be deleted by a call to [IDebugBoundBreakpoint2::Delete](../vs140/IDebugBoundBreakpoint2--Delete.md).  
  
## See Also  
 [Calling Debugger Events](../vs140/Calling-Debugger-Events.md)