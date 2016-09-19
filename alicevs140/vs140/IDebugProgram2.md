---
title: "IDebugProgram2"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 8d73df73-cfff-4b8b-b426-d6051edb1939
caps.latest.revision: 20
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugProgram2
This interface represents a program that is running in a process.  
  
## Syntax  
  
```  
IDebugProgram2 : IUnknown  
```  
  
## Notes for Implementers  
 The debug engine (DE) and a custom port supplier implement this interface to represent a program in a process. The session debug manager (SDM) also implements this interface to provide information to [IDebugProgram2::Attach](../vs140/IDebugProgram2--Attach.md).  
  
## Notes for Callers  
 The [IDebugProgramCreateEvent2](../vs140/IDebugProgramCreateEvent2.md) event returns this interface for a new program. This interface is also used as a parameter for many methods on multiple interfaces.  
  
## Methods in Vtable Order  
 The following table shows the methods of `IDebugProgram2`.  
  
|Method|Description|  
|------------|-----------------|  
|[EnumThreads](../vs140/IDebugProgram2--EnumThreads.md)|Enumerates the threads that are running in this program.|  
|[GetName](../vs140/IDebugProgram2--GetName.md)|Gets the name of the program.|  
|[GetProcess](../vs140/IDebugProgram2--GetProcess.md)|Gets the process that this program is running in.|  
|[Terminate](../vs140/IDebugProgram2--Terminate.md)|Terminates this program.|  
|[Attach](../vs140/IDebugProgram2--Attach.md)|Attaches to this program.|  
|[CanDetach](../vs140/IDebugProgram2--CanDetach.md)|Determines if a debug engine (DE) can detach from the program.|  
|[Detach](../vs140/IDebugProgram2--Detach.md)|Detaches the debugger from this program.|  
|[GetProgramId](../vs140/IDebugProgram2--GetProgramId.md)|Gets a globally unique identifier for this program.|  
|[GetDebugProperty](../vs140/IDebugProgram2--GetDebugProperty.md)|Gets program properties.|  
|[Execute](../vs140/IDebugProgram2--Execute.md)|Continues running this program from a stopped state. Any previous execution state is cleared.|  
|[Continue](../vs140/IDebugProgram2--Continue.md)|Continues running this program from a stopped state. Any previous execution state is preserved.|  
|[Step](../vs140/IDebugProgram2--Step.md)|Performs a step.|  
|[CauseBreak](../vs140/IDebugProgram2--CauseBreak.md)|Requests that this program stop execution the next time one of its threads runs code.|  
|[GetEngineInfo](../vs140/IDebugProgram2--GetEngineInfo.md)|Gets the name and identifier of the debug engine (DE) running this program.|  
|[EnumCodeContexts](../vs140/IDebugProgram2--EnumCodeContexts.md)|Enumerates the code contexts for a given position in a source file.|  
|[GetMemoryBytes](../vs140/IDebugProgram2--GetMemoryBytes.md)|Gets the memory bytes for this program.|  
|[GetDisassemblyStream](../vs140/IDebugProgram2--GetDisassemblyStream.md)|Gets the disassembly stream for this program or part of this program.|  
|[EnumModules](../vs140/IDebugProgram2--EnumModules.md)|Enumerates the modules that this program has loaded and is executing.|  
|[GetENCUpdate](../vs140/IDebugProgram2--GetENCUpdate.md)|Gets the Edit and Continue (ENC) update for this program.<br /><br /> A custom debug engine does not implement this method (it should always return `E_NOTIMPL`).|  
|[EnumCodePaths](../vs140/IDebugProgram2--EnumCodePaths.md)|Enumerates the code paths of this program.|  
|[WriteDump](../vs140/IDebugProgram2--WriteDump.md)|Writes a dump to a file.|  
  
## Requirements  
 Header: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## Remarks  
 A program is a thread container running in a particular run-time architecture, while a process is made up of one or more programs.  
  
## See Also  
 [Core Interfaces](../vs140/Core-Interfaces.md)   
 [GetProgram](../vs140/IDebugThread2--GetProgram.md)   
 [Next](../vs140/IEnumDebugPrograms2--Next.md)   
 [Event](../vs140/IDebugPortEvents2--Event.md)   
 [Attach](../vs140/IDebugEngine2--Attach.md)   
 [DestroyProgram](../vs140/IDebugEngine2--DestroyProgram.md)   
 [Event](../vs140/IDebugEventCallback2--Event.md)   
 [Attach_V7](../vs140/IDebugProgramNode2--Attach_V7.md)