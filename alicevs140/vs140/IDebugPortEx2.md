---
title: "IDebugPortEx2"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 144724d0-38ee-4c9b-87ca-8a504371182b
caps.latest.revision: 15
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugPortEx2
This interface lets the session debug manager (SDM) control the programs and processes running on a port.  
  
## Syntax  
  
```  
IDebugPortEx2 : IUnknown  
```  
  
## Notes for Implementers  
 A custom port supplier implements this interface on the same object that implements [IDebugPort2](../vs140/IDebugPort2.md).  
  
## Notes for Callers  
 The SDM calls [QueryInterface](../vs140/QueryInterface.md) on the `IDebugPort2` interface to obtain this interface.  
  
## Methods in Vtable Order  
 The following table shows the methods of `IDebugPortEx2`.  
  
|Method|Description|  
|------------|-----------------|  
|[LaunchSuspended](../vs140/IDebugPortEx2--LaunchSuspended.md)|Launches an executable file.|  
|[ResumeProcess](../vs140/IDebugPortEx2--ResumeProcess.md)|Resumes execution of a process.|  
|[CanTerminateProcess](../vs140/IDebugPortEx2--CanTerminateProcess.md)|Determines whether a process can be terminated.|  
|[TerminateProcess](../vs140/IDebugPortEx2--TerminateProcess.md)|Terminates a process.|  
|[GetPortProcessId](../vs140/IDebugPortEx2--GetPortProcessId.md)|Gets the process ID of the port itself.|  
|[GetProgram](../vs140/IDebugPortEx2--GetProgram.md)|Gets a program associated with a program node.|  
  
## Remarks  
 This interface is normally private between the SDM and the custom port supplier.  
  
 If desired, a debug engine (DE) can look for this interface on the [IDebugPort2](../vs140/IDebugPort2.md) interface passed to [IDebugEngineLaunch2::LaunchSuspended](../vs140/IDebugEngineLaunch2--LaunchSuspended.md) and use [IDebugPortEx2::LaunchSuspended](../vs140/IDebugPortEx2--LaunchSuspended.md) to launch the program. This is not a requirement, however, and a DE can do whatever it needs to do to launch the request program.  
  
## Requirements  
 Header: portpriv.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [Core Interfaces](../vs140/Core-Interfaces.md)   
 [IDebugPort2](../vs140/IDebugPort2.md)