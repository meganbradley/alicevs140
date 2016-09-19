---
title: "IDebugProgramDestroyEvent2"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: ddf127ca-c4a5-4071-90ca-68faf2f57dbd
caps.latest.revision: 13
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugProgramDestroyEvent2
This interface is sent by the debug engine (DE) to the session debug manager (SDM) when a program has run to completion.  
  
## Syntax  
  
```  
IDebugProgramDestroyEvent2 : IUnknown  
```  
  
## Notes for Implementers  
 The DE or the custom port supplier implements this interface to report that a program has been terminated and is no longer available for debugging. The [IDebugEvent2](../vs140/IDebugEvent2.md) interface must be implemented on the same object as this interface. The SDM uses [QueryInterface](../vs140/QueryInterface.md) to access the `IDebugEvent2` interface.  
  
## Notes for Callers  
 The DE or the custom port supplier creates and sends this event object to report the termination of a program. The DE sends this event by using the [IDebugEventCallback2](../Topic/IDebugEventCallback2.md) callback function that is supplied by the SDM when it attached to the program being debugged. The custom port supplier sends this event using the [IDebugPortEvents2](../Topic/IDebugPortEvents2.md) interface.  
  
## Methods in Vtable Order  
 The following table shows the method of `IDebugProgramDestroyEvent2`.  
  
|Method|Description|  
|------------|-----------------|  
|[GetExitCode](../vs140/IDebugProgramDestroyEvent2--GetExitCode.md)|Gets the program's exit code.|  
  
## Requirements  
 Header: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [Core Interfaces](../vs140/Core-Interfaces.md)   
 [IDebugProgram2](../vs140/IDebugProgram2.md)   
 [IDebugEvent2](../vs140/IDebugEvent2.md)   
 [IDebugEventCallback2](../Topic/IDebugEventCallback2.md)