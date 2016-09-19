---
title: "IDebugFirewallConfigurationCallback2"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 0827361c-b97c-4851-9898-ab6d88c81811
caps.latest.revision: 10
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugFirewallConfigurationCallback2
Enables a debug engine that uses DCOM to ask the [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] UI to make sure that the firewall will not block remote debugging.  
  
## Syntax  
  
```  
IDebugFirewallConfigurationCallback2 : IUnknown  
```  
  
## Notes for Implementers  
 Implemented by the port object of the session debug manager.  
  
## Methods  
 The following table shows the methods of `IDebugFirewallConfigurationCallback2`.  
  
|Method|Description|  
|------------|-----------------|  
|[IDebugFirewallConfigurationCallback2:: EnsureDCOMUnblocked](../vs140/IDebugFirewallConfigurationCallback2--EnsureDCOMUnblocked.md)|Requests that the firewall not block remote debugging.|  
  
## Requirements  
 Header: Msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll