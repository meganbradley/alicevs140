---
title: "IDebugProgram3"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 4301ba23-c00c-4ce5-8b1e-3f27da312034
caps.latest.revision: 7
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugProgram3
This interface represents a program that is running in a process and extends [IDebugProgram2::Execute](../vs140/IDebugProgram2--Execute.md) by providing thread information.  
  
## Syntax  
  
```  
IDebugProgram3 : IDebugProgram3  
```  
  
## Notes for Implementers  
 The debug engine (DE) and a custom port supplier implement this interface to represent a program in a process. The session debug manager (SDM) also implements this interface to provide information to [IDebugProgram2::Attach](../vs140/IDebugProgram2--Attach.md).  
  
## Notes for Callers  
 The [IDebugProgramCreateEvent2](../vs140/IDebugProgramCreateEvent2.md) event returns this interface for a new program. This interface is also used as a parameter for many methods on multiple interfaces.  
  
## Methods in Vtable Order  
 The following table shows the methods of `IDebugProgram3`.  
  
|Method|Description|  
|------------|-----------------|  
|[IDebugProgram3::ExecuteOnThread](../vs140/IDebugProgram3--ExecuteOnThread.md)|Executes the program. The thread is returned to give the debugger information on which thread the user is viewing when executing.|  
  
## Requirements  
 Header: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## Remarks  
 A program is a thread container running in a particular run-time architecture, while a process is made up of one or more programs.  
  
## See Also  
 [Core Interfaces](../vs140/Core-Interfaces.md)   
 [IDebugProgram2](../vs140/IDebugProgram2.md)   
 [GetProgram](../vs140/IDebugThread2--GetProgram.md)   
 [Next](../vs140/IEnumDebugPrograms2--Next.md)   
 [Event](../vs140/IDebugPortEvents2--Event.md)   
 [Attach](../vs140/IDebugEngine2--Attach.md)   
 [DestroyProgram](../vs140/IDebugEngine2--DestroyProgram.md)   
 [Event](../vs140/IDebugEventCallback2--Event.md)   
 [Attach_V7](../vs140/IDebugProgramNode2--Attach_V7.md)