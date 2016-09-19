---
title: "IDebugProcessEx2"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 44e309ba-1d6f-499b-aa7e-9b34858a6d57
caps.latest.revision: 23
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugProcessEx2
This interface lets the session debug manager (SDM) notify a process that it is attaching to or detaching from the process.  
  
## Syntax  
  
```  
IDebugProcessEx2 : IUnknown  
```  
  
## Notes for Implementers  
 A custom port supplier implements this interface on the same object as the [IDebugProcess2](../vs140/IDebugProcess2.md) interface in order to:  
  
-   Support tracking of sessions connected to a process  
  
-   Support auto-attach across multiple debug engines  
  
 The custom port supplier can implement this interface if it chooses.  
  
## Notes for Callers  
  
-   The SDM calls [QueryInterface](../vs140/QueryInterface.md) on an `IDebugProcess2` interface to obtain this interface.  
  
## Methods in Vtable Order  
 The following table shows the methods of `IDebugProcessEx2`.  
  
|Method|Description|  
|------------|-----------------|  
|[Attach](../vs140/IDebugProcessEx2--Attach.md)|Informs the process that a session is now debugging the process.|  
|[Detach](../vs140/IDebugProcessEx2--Detach.md)|Informs the process that a session is no longer debugging the process.|  
|[AddImplicitProgramNodes](../vs140/IDebugProcessEx2--AddImplicitProgramNodes.md)|Adds program nodes for a list of debug engines.|  
  
## Remarks  
 This interface is private between the SDM and the process.  
  
## Requirements  
 Header: Portpriv.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [Core Interfaces](../vs140/Core-Interfaces.md)   
 [IDebugProcess2](../vs140/IDebugProcess2.md)