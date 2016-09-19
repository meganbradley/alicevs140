---
title: "IDebugThreadDestroyEvent2"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: fca3f603-9432-457b-9ddd-8b0ec17da046
caps.latest.revision: 13
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugThreadDestroyEvent2
This interface is sent by the debug engine (DE) to the session debug manager (SDM) when a thread has run to completion.  
  
## Syntax  
  
```  
IDebugThreadDestroyEvent2 : IUnknown  
```  
  
## Notes for Implementers  
 The DE implements this interface to report that a thread has ended. The [IDebugEvent2](../vs140/IDebugEvent2.md) interface must be implemented on the same object as this interface. The SDM uses [QueryInterface](../vs140/QueryInterface.md) to access the `IDebugEvent2` interface.  
  
## Notes for Callers  
 The DE creates and sends this event object to report that a thread has ended. The event is sent by using the [IDebugEventCallback2](../Topic/IDebugEventCallback2.md) callback function that is supplied by the SDM when it is attached to the program being debugged.  
  
## Methods in Vtable Order  
 The following table shows the methods of `IDebugThreadDestroyEvent2`.  
  
|Method|Description|  
|------------|-----------------|  
|[GetExitCode](../vs140/IDebugThreadDestroyEvent2--GetExitCode.md)|Gets the thread's exit code.|  
  
## Remarks  
 Visual Studio uses this event to update the **Threads** window.  
  
## Requirements  
 Header: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [Core Interfaces](../vs140/Core-Interfaces.md)   
 [IDebugThread2](../vs140/IDebugThread2.md)   
 [IDebugEvent2](../vs140/IDebugEvent2.md)   
 [IDebugEventCallback2](../Topic/IDebugEventCallback2.md)