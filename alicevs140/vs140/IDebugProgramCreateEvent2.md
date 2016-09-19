---
title: "IDebugProgramCreateEvent2"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: b19a7934-6179-4a68-9075-bd7dcd640b05
caps.latest.revision: 15
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugProgramCreateEvent2
This interface is sent by the debug engine (DE) to the session debug manager (SDM) when a program is attached to.  
  
## Syntax  
  
```  
IDebugProgramCreateEvent2 : IUnknown  
```  
  
## Notes for Implementers  
 The DE or the custom port supplier implements this interface to report that a program has been created, typically at the time the program is attached to. The [IDebugEvent2](../vs140/IDebugEvent2.md) interface must be implemented on the same object as this interface. The SDM uses the `QueryInterface` method to access the `IDebugEvent2` interface.  
  
## Notes for Callers  
 The DE or the custom port supplier creates and sends this event object to report the creation of a program. The DE sends this event by using the [IDebugEventCallback2](../Topic/IDebugEventCallback2.md) callback function that is supplied by the SDM when it attached to the program being debugged. The custom port supplier sends this event using the [IDebugPortEvents2](../Topic/IDebugPortEvents2.md) interface.  
  
## Remarks  
 The DE or custom port supplier publishes a new [IDebugProgramNode2](../vs140/IDebugProgramNode2.md) interface by calling [IDebugProgramPublisher2::PublishProgramNode](../vs140/IDebugProgramPublisher2--PublishProgramNode.md).  
  
## Requirements  
 Header: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [Core Interfaces](../vs140/Core-Interfaces.md)   
 [IDebugEvent2](../vs140/IDebugEvent2.md)   
 [IDebugEventCallback2](../Topic/IDebugEventCallback2.md)   
 [IDebugPortEvents2](../Topic/IDebugPortEvents2.md)   
 [IDebugProgram2](../vs140/IDebugProgram2.md)