---
title: "IDebugPort2"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 8fd87f05-a950-4d14-b925-98be29d4facc
caps.latest.revision: 15
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugPort2
This interface represents a debug port on a machine.  
  
## Syntax  
  
```  
IDebugPort2 : IUnknown  
```  
  
## Notes for Implementers  
 A custom port supplier implements this interface to represent a debug port on a machine.  
  
 If the port supports sending port events, it must also implement the <xref:System.Runtime.InteropServices.ComTypes.IConnectionPointContainer?qualifyHint=False> interface to support an <xref:System.Runtime.InteropServices.ComTypes.IConnectionPoint?qualifyHint=False> interface that in turn provides the [IDebugPortEvents2](../Topic/IDebugPortEvents2.md) interface.  
  
## Notes for Callers  
 Calls to [IDebugPortSupplier2::GetPort](../vs140/IDebugPortSupplier2--GetPort.md) or [IDebugPortSupplier2::AddPort](../vs140/IDebugPortSupplier2--AddPort.md) return this interface, representing the requested port.  
  
## Methods in Vtable Order  
 The following table shows the methods of `IDebugPort2`.  
  
|Method|Description|  
|------------|-----------------|  
|[GetPortName](../vs140/IDebugPort2--GetPortName.md)|Returns the port name.|  
|[GetPortId](../vs140/IDebugPort2--GetPortId.md)|Returns the port identifier.|  
|[GetPortRequest](../vs140/IDebugPort2--GetPortRequest.md)|Returns the request used to create a port (if available).|  
|[GetPortSupplier](../vs140/IDebugPort2--GetPortSupplier.md)|Returns the port supplier for this port.|  
|[GetProcess](../vs140/IDebugPort2--GetProcess.md)|Returns an interface to the process given the process's identifier.|  
|[EnumProcesses](../vs140/IDebugPort2--EnumProcesses.md)|Enumerates all the processes running on a port.|  
  
## Remarks  
 The local port provides access to all the processes and programs running on the local machine. Other ports might represent a serial cable connection to a Windows CE-based device, or a network connection to a non-DCOM computer. The `IDebugPort2` interface is used to find the name and identifier of a port, enumerate all processes running on the port, and provide facilities for launching and terminating processes on the port.  
  
## Requirements  
 Header: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [Core Interfaces](../vs140/Core-Interfaces.md)   
 [IDebugPortSupplier2](../vs140/IDebugPortSupplier2.md)   
 [IDebugCoreServer2](../vs140/IDebugCoreServer2.md)