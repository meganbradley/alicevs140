---
title: "IDebugEngineLaunch2"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 5eaf2ad8-3fbf-446e-b48b-5327ad3f5255
caps.latest.revision: 14
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugEngineLaunch2
Used by a debug engine (DE) to launch and terminate programs.  
  
## Syntax  
  
```  
IDebugEngineLaunch2 : IDebugEngine2  
```  
  
## Notes for Implementers  
 This interface is implemented by a custom DE if it has special requirements for launching a process that cannot be handled entirely by a custom port. This is typically the case when the DE is part of an interpreter and the process being debugged is a script: the interpreter needs to be launched first, and then the script is loaded and started. A port can launch the interpreter, but the script may require special handling (which is where the DE has a role). This interface is implemented only if there are unique requirements for launching a program that a custom port cannot handle.  
  
## Notes for Callers  
 This interface is called by the session debug manager (SDM) if the SDM can get this interface from the [IDebugEngine2](../vs140/IDebugEngine2.md) interface (using QueryInterface). If this interface can be obtained, the SDM knows that the DE has special requirements and calls this interface to launch the program instead of having the port launch it.  
  
## Methods in Vtable Order  
 The following table shows the methods of `IDebugEngineLaunch2`.  
  
|Method|Description|  
|------------|-----------------|  
|[LaunchSuspended](../vs140/IDebugEngineLaunch2--LaunchSuspended.md)|Launches a process by means of the DE.|  
|[ResumeProcess](../vs140/IDebugEngineLaunch2--ResumeProcess.md)|Resumes process execution.|  
|[CanTerminateProcess](../vs140/IDebugEngineLaunch2--CanTerminateProcess.md)|Determines if a process can be terminated.|  
|[TerminateProcess](../vs140/IDebugEngineLaunch2--TerminateProcess.md)|Terminates a process.|  
  
## Requirements  
 Header: Msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [IDebugEngine2](../vs140/IDebugEngine2.md)