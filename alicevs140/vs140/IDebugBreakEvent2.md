---
title: "IDebugBreakEvent2"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 57dfdbc2-4e68-4dbf-9579-006cd6fb1c62
caps.latest.revision: 15
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugBreakEvent2
This interface tells the session debug manager (SDM) that an asynchronous break has been successfully completed.  
  
## Syntax  
  
```  
IDebugBreakEvent2 : IUnknown  
```  
  
## Notes for Implementers  
 The DE implements this interface to support user breaks in a program. The [IDebugEvent2](../vs140/IDebugEvent2.md) interface must be implemented on the same object as this interface (the SDM uses [QueryInterface](../vs140/QueryInterface.md) to access the `IDebugEvent2` interface).  
  
## Notes for Callers  
 The SDM calls [IDebugProgram2::CauseBreak](../vs140/IDebugProgram2--CauseBreak.md) when the user has requested the program being debugged to be paused. When the program has successfully been paused, the DE sends the `IDebugBreakEvent2` event. This event is sent by using the [IDebugEventCallback2](../Topic/IDebugEventCallback2.md) callback function supplied by the SDM when it attached to the program being debugged.  
  
## Remarks  
 For example, a user can select the **Break All** command on the **Debug** menu to break out of a program that is running an infinite loop. The SDM tells the program to stop by calling [CauseBreak](../vs140/IDebugProgram2--CauseBreak.md). The DE sends `IDebugBreakEvent2` when the program finally stops.  
  
## Requirements  
 Header: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [CauseBreak](../vs140/IDebugProgram2--CauseBreak.md)   
 [IDebugEvent2](../vs140/IDebugEvent2.md)   
 [IDebugEventCallback2](../Topic/IDebugEventCallback2.md)