---
title: "IDebugCoreServer3"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 51f5f41b-a5a4-4df0-a703-41f3d1811d7f
caps.latest.revision: 10
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugCoreServer3
This interface gives access to information about the server the process is running in.  
  
## Syntax  
  
```  
IDebugCoreServer3 : IDebugCoreServer2  
```  
  
## Notes for Implementers  
 Visual Studio implements this interface.  
  
## Notes for Callers  
 Use [QueryInterface](../vs140/QueryInterface.md) to obtain this interface from an [IDebugCoreServer2](../vs140/IDebugCoreServer2.md) interface. A call to [IDebugDefaultPort2::GetServer](../vs140/IDebugDefaultPort2--GetServer.md) can also return this interface. This interface is used most often by a custom port supplier to launch programs on a server (either local or remote).  
  
## Methods in Vtable Order  
 In addition to the methods on the [IDebugCoreServer2](../vs140/IDebugCoreServer2.md) interface, this interface implements the following methods:  
  
|Method|Description|  
|------------|-----------------|  
|[GetServerName](../vs140/IDebugCoreServer3--GetServerName.md)|Retrieves the name of the server.|  
|[GetServerFriendlyName](../vs140/IDebugCoreServer3--GetServerFriendlyName.md)|Retrieves a friendly version of the server name|  
|[EnableAutoAttach](../vs140/IDebugCoreServer3--EnableAutoAttach.md)|Tells specific debug engines to automatically attach to processes when those processes start.|  
|[DiagnoseWebDebuggingError](../vs140/IDebugCoreServer3--DiagnoseWebDebuggingError.md)|Retrieves a specific error code when automatic attach fails.|  
|[CreateInstanceInServer](../vs140/IDebugCoreServer3--CreateInstanceInServer.md)|Creates an instance of a debug engine on the server.|  
|[QueryIsLocal](../vs140/IDebugCoreServer3--QueryIsLocal.md)|Retrieves a flag indicating whether the server is on the same machine as the caller.|  
|[GetConnectionProtocol](../vs140/IDebugCoreServer3--GetConnectionProtocol.md)|Retrieves a value indicating the protocol being used to communicate with the server.|  
|[DisableAutoAttach](../vs140/IDebugCoreServer3--DisableAutoAttach.md)|Disables all auto-attach settings for all debug engines this server knows about.|  
  
## Remarks  
 A custom port supplier receives the [IDebugCoreServer2](../vs140/IDebugCoreServer2.md) interface on a call to [IDebugPortEvents2::Event](../vs140/IDebugPortEvents2--Event.md). The `IDebugCoreServer3` interface can be obtained from that interface.  
  
## Requirements  
 Header: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [IDebugCoreServer2](../vs140/IDebugCoreServer2.md)   
 [IDebugDefaultPort2::GetServer](../vs140/IDebugDefaultPort2--GetServer.md)