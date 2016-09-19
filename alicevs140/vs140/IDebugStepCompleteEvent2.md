---
title: "IDebugStepCompleteEvent2"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: eba2b76e-f90d-486b-ae5c-c47f1b8ba2e5
caps.latest.revision: 13
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugStepCompleteEvent2
This interface is sent by the debug engine (DE) to the session debug manager (SDM) when the program being debugged completes a step into, a step over, or a step out of a line of source code or statement or instruction.  
  
## Syntax  
  
```  
IDebugStepCompleteEvent2 : IUnknown  
```  
  
## Notes for Implementers  
 The DE implements this interface to report the completion of a step operation. The [IDebugEvent2](../vs140/IDebugEvent2.md) interface must be implemented on the same object as this interface. The SDM uses [QueryInterface](../vs140/QueryInterface.md) to access the `IDebugEvent2` interface.  
  
## Notes for Callers  
 The DE creates and sends this event object to report the completion of a step operation. The event is sent by using the [IDebugEventCallback2](../Topic/IDebugEventCallback2.md) callback function that is supplied by the SDM when it is attached to the program being debugged.  
  
## Remarks  
 Once the step has been completed, the program being debugged is paused once more, and the IDE updates all its windows.  
  
## Requirements  
 Header: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [Core Interfaces](../vs140/Core-Interfaces.md)   
 [IDebugEvent2](../vs140/IDebugEvent2.md)   
 [IDebugEventCallback2](../Topic/IDebugEventCallback2.md)