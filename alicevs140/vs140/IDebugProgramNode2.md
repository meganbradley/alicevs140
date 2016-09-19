---
title: "IDebugProgramNode2"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 80e511d8-9b40-4a85-aa5d-952fa5ee6ae7
caps.latest.revision: 22
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugProgramNode2
This interface represents a program that can be debugged.  
  
## Syntax  
  
```  
IDebugProgramNode2 : IUnknown  
```  
  
## Notes for Implementers  
 A debug engine (DE) or a custom port supplier implements this interface to represent a program that can be debugged. This interface is typically implemented on the same object that implements the [IDebugProgram2](../vs140/IDebugProgram2.md) interface. This interface is registered with [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] by calling [IDebugProgramPublisher2::PublishProgramNode](../vs140/IDebugProgramPublisher2--PublishProgramNode.md).  
  
## Notes for Callers  
 Call [IDebugProgramProvider2::GetProviderProgramNode](../vs140/IDebugProgramProvider2--GetProviderProgramNode.md) to return this interface. A custom port supplier receives this interface through a call to [IDebugPortNotify2::AddProgramNode](../vs140/IDebugPortNotify2--AddProgramNode.md). A DE receives this interface through a call to [IDebugEngine2::Attach](../vs140/IDebugEngine2--Attach.md).  
  
## Methods in Vtable Order  
 The following table shows the methods of `IDebugProgramNode2`.  
  
|Method|Description|  
|------------|-----------------|  
|[GetProgramName](../vs140/IDebugProgramNode2--GetProgramName.md)|Gets the name of a program.|  
|[GetHostName](../vs140/IDebugProgramNode2--GetHostName.md)|Gets the name of the process hosting a program.|  
|[GetHostPid](../vs140/IDebugProgramNode2--GetHostPid.md)|Gets the system process identifier for the process hosting a program.|  
|[GetHostMachineName_V7](../vs140/IDebugProgramNode2--GetHostMachineName_V7.md)|DEPRECATED. DO NOT USE.|  
|[Attach_V7](../vs140/IDebugProgramNode2--Attach_V7.md)|DEPRECATED. DO NOT USE. See the [IDebugProgramNodeAttach2](../vs140/IDebugProgramNodeAttach2.md) interface for an alternative approach.|  
|[GetEngineInfo](../vs140/IDebugProgramNode2--GetEngineInfo.md)|Gets the name and identifier of the DE running this program.|  
|[DetachDebugger_V7](../vs140/IDebugProgramNode2--DetachDebugger_V7.md)|DEPRECATED. DO NOT USE.|  
  
## Remarks  
 The session debug manager (SDM) typically calls [IDebugProgramProvider2::GetProviderProgramNode](../vs140/IDebugProgramProvider2--GetProviderProgramNode.md) to obtain this interface.  
  
## Requirements  
 Header: Msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [Core Interfaces](../vs140/Core-Interfaces.md)   
 [IDebugProgramNodeAttach2](../vs140/IDebugProgramNodeAttach2.md)   
 [AddProgramNode](../vs140/IDebugPortNotify2--AddProgramNode.md)   
 [RemoveProgramNode](../vs140/IDebugPortNotify2--RemoveProgramNode.md)   
 [IDebugEngine2::Attach](../vs140/IDebugEngine2--Attach.md)   
 [IDebugProgramProvider2::GetProviderProgramNode](../vs140/IDebugProgramProvider2--GetProviderProgramNode.md)   
 [IDebugProgramPublisher2::PublishProgramNode](../vs140/IDebugProgramPublisher2--PublishProgramNode.md)