---
title: "IEnumDebugPorts2"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 1754eef3-cf62-42e0-b218-1911acba77d4
caps.latest.revision: 14
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IEnumDebugPorts2
This interface enumerates the ports of a machine or port supplier.  
  
## Syntax  
  
```  
IEnumDebugPorts2 : IUnknown  
```  
  
## Notes for Implementers  
 A custom port supplier implements this interface to represent a list of ports created by the supplier. Visual Studio implements this interface in support of its own port supplier.  
  
## Notes for Callers  
 Call [IDebugPortSupplier2::EnumPorts](../vs140/IDebugPortSupplier2--EnumPorts.md) to obtain this interface representing a list of ports created by the port supplier. Call [IDebugPortSupplier3::EnumPersistedPorts](../vs140/IDebugPortSupplier3--EnumPersistedPorts.md) to obtain this interface representing a list of ports that were saved to disk.  
  
## Methods in Vtable Order  
 The following table shows the methods of `IEnumDebugPorts2`.  
  
|Method|Description|  
|------------|-----------------|  
|[Next](../vs140/IEnumDebugPorts2--Next.md)|Retrieves a specified number of ports in an enumeration sequence.|  
|[Skip](../vs140/IEnumDebugPorts2--Skip.md)|Skips a specified number of ports in an enumeration sequence.|  
|[Reset](../vs140/IEnumDebugPorts2--Reset.md)|Resets an enumeration sequence to the beginning.|  
|[Clone](../vs140/IEnumDebugPorts2--Clone.md)|Creates an enumerator that contains the same enumeration state as the current enumerator.|  
|[GetCount](../vs140/IEnumDebugPorts2--GetCount.md)|Gets the number of ports in an enumerator.|  
  
## Remarks  
 Visual Studio uses this interface to help populate a list of ports used for attaching to processes.  
  
 A debug engine typically does not use this interface.  
  
## Requirements  
 Header: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [Core Interfaces](../vs140/Core-Interfaces.md)   
 [EnumPorts](../vs140/IDebugCoreServer2--EnumPorts.md)   
 [EnumPorts](../vs140/IDebugPortSupplier2--EnumPorts.md)