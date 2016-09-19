---
title: "IDebugEngine2"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 1f0e9ac0-6dfb-461a-976c-888d82144cdb
caps.latest.revision: 17
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugEngine2
This interface represents a debug engine (DE). It is used to manage various aspects of a debugging session, from creating breakpoints to setting and clearing exceptions.  
  
## Syntax  
  
```  
IDebugEngine2 : IUnknown  
```  
  
## Notes for Implementers  
 This interface is implemented by a custom DE to manage debugging of programs. This interface must be implemented by the DE.  
  
## Notes for Callers  
 This interface is called by the session debug manager (SDM) to manage the debugging session, including managing exceptions, creating breakpoints, and responding to synchronous events sent by the DE.  
  
## Methods in Vtable Order  
 The following table shows the methods of `IDebugEngine2`.  
  
|Method|Description|  
|------------|-----------------|  
|[EnumPrograms](../vs140/IDebugEngine2--EnumPrograms.md)|Creates an enumerator for all the programs being debugged by a DE.|  
|[Attach](../vs140/IDebugEngine2--Attach.md)|Attaches a DE to a program.|  
|[CreatePendingBreakpoint](../vs140/IDebugEngine2--CreatePendingBreakpoint.md)|Creates a pending breakpoint in the DE.|  
|[SetException](../vs140/IDebugEngine2--SetException.md)|Specifies how the DE should handle a given exception.|  
|[RemoveSetException](../vs140/IDebugEngine2--RemoveSetException.md)|Removes the specified exception so it is no longer handled by the debug engine.|  
|[RemoveAllSetExceptions](../vs140/IDebugEngine2--RemoveAllSetExceptions.md)|Removes the list of exceptions the IDE has set for a particular run-time architecture or language.|  
|[GetEngineID](../vs140/IDebugEngine2--GetEngineID.md)|Gets the GUID of the DE.|  
|[DestroyProgram](../vs140/IDebugEngine2--DestroyProgram.md)|Informs a DE that the program specified has been atypically terminated and that the DE should clean up all references to the program and send a program destroy event.|  
|[ContinueFromSynchronousEvent](../vs140/IDebugEngine2--ContinueFromSynchronousEvent.md)|Called by the SDM to indicate that a synchronous debug event, previously sent by the DE to the SDM, was received and processed.|  
|[SetLocale](../vs140/IDebugEngine2--SetLocale.md)|Sets the locale of the DE.|  
|[SetRegistryRoot](../vs140/IDebugEngine2--SetRegistryRoot.md)|Sets the registry root currently in use by the DE.|  
|[SetMetric](../vs140/IDebugEngine2--SetMetric.md)|Sets a metric.|  
|[CauseBreak](../vs140/IDebugEngine2--CauseBreak.md)|Requests that all programs being debugged by this DE stop execution the next time one of their threads attempts to run.|  
  
## Requirements  
 Header: Msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [Event](../vs140/IDebugEventCallback2--Event.md)   
 [GetEngine](../vs140/IDebugEngineCreateEvent2--GetEngine.md)