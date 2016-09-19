---
title: "IDebugCoreServer2"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 9c47d0a6-9eb1-464e-bd44-fa2b552d4d36
caps.latest.revision: 16
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugCoreServer2
This interface is used to represent and obtain information from a server on a machine on the network.  
  
## Syntax  
  
```  
IDebugCoreServer2 : IUknown  
```  
  
## Notes for Implementers  
 Visual Studio implements this interface to represent a server. Each instance of Visual Studio creates an instance of this interface.  
  
## Notes for Callers  
 A custom port supplier receives this interface in a call to [IDebugPortEvents2::Event](../vs140/IDebugPortEvents2--Event.md).  
  
 A debug engine can obtain this interface indirectly through a call to [IDebugDefaultPort2::GetServer](../vs140/IDebugDefaultPort2--GetServer.md) (which returns [IDebugCoreServer3](../vs140/IDebugCoreServer3.md), an interface that is derived from `IDebugCoreServer2`).  
  
## Methods in Vtable Order  
 The following table shows the methods of `IDebugCoreServer2`.  
  
|Method|Description|  
|------------|-----------------|  
|[GetMachineInfo](../vs140/IDebugCoreServer2--GetMachineInfo.md)|Gets the name and attributes of a machine.|  
|[GetMachineName](../vs140/IDebugCoreServer2--GetMachineName.md)|Gets the name of a machine.|  
|[GetPortSupplier](../vs140/IDebugCoreServer2--GetPortSupplier.md)|Gets a port supplier that exists on a machine.|  
|[GetPort](../vs140/IDebugCoreServer2--GetPort.md)|Gets a port that already exists on a machine.|  
|[EnumPorts](../vs140/IDebugCoreServer2--EnumPorts.md)|Creates an enumerator for all the ports on a machine.|  
|[EnumPortSuppliers](../vs140/IDebugCoreServer2--EnumPortSuppliers.md)|Creates an enumerator for all the port suppliers on a machine.|  
|[GetMachineUtilities_V7](../vs140/IDebugCoreServer2--GetMachineUtilities_V7.md)|Gets the machine utilities for a machine.|  
  
## Remarks  
 This interface is also used by Visual Studio to browse processes running on machines on the network.  
  
## Requirements  
 Header: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [IDebugPort2](../vs140/IDebugPort2.md)   
 [IDebugPortEvents2::Event](../vs140/IDebugPortEvents2--Event.md)   
 [IDebugDefaultPort2::GetServer](../vs140/IDebugDefaultPort2--GetServer.md)   
 [IDebugCoreServer3](../vs140/IDebugCoreServer3.md)