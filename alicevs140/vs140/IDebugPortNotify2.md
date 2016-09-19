---
title: "IDebugPortNotify2"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 43278b79-bf16-4c08-bcf1-6f7f7a17feab
caps.latest.revision: 13
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugPortNotify2
This interface registers or unregisters a program that can be debugged with the port it is running on.  
  
## Syntax  
  
```  
IDebugPortNotify2 : IUnknown  
```  
  
## Notes for Implementers  
 A custom port supplier implements this interface to support adding and removing programs from the port. It is typically implemented on the same object that implements the [IDebugPort2](../vs140/IDebugPort2.md) interface.  
  
## Notes for Callers  
 A call to [QueryInterface](../vs140/QueryInterface.md) on the `IDebugPort2` interface returns this interface. Also, a call to [IDebugDefaultPort2::GetPortNotify](../vs140/IDebugDefaultPort2--GetPortNotify.md) returns this interface. A debug engine can see this interface as a parameter to [IDebugProgramProvider2::WatchForProviderEvents](../vs140/IDebugProgramProvider2--WatchForProviderEvents.md).  
  
## Methods in Vtable Order  
 The following table shows the methods of `IDebugPortNotify2`.  
  
|Method|Description|  
|------------|-----------------|  
|[AddProgramNode](../vs140/IDebugPortNotify2--AddProgramNode.md)|Registers a program that can be debugged with the port it is running on.|  
|[RemoveProgramNode](../vs140/IDebugPortNotify2--RemoveProgramNode.md)|Unregisters a program that can be debugged from the port it is running on.|  
  
## Remarks  
 Unless a debug port has a way to know when programs are loaded or unloaded, a custom port supplier must implement this interface. All programs that are loaded for debugging through a particular port are tracked using this interface.  
  
## Requirements  
 Header: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [Core Interfaces](../vs140/Core-Interfaces.md)   
 [IDebugProgramNode2](../vs140/IDebugProgramNode2.md)