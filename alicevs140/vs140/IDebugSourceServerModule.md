---
title: "IDebugSourceServerModule"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 38213060-451d-46e6-8b4a-efc123e01a2c
caps.latest.revision: 10
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugSourceServerModule
Represents the source server information that is contained in a PDB file.  
  
## Syntax  
  
```  
IDebugSourceServerModule : IUnknown  
```  
  
## Notes for Implementers  
 This interface is implemented by debugger engines and consumed by the debugger UI.  
  
## Methods  
 The following table shows the methods of `IDebugSourceServerModule`.  
  
|Method|Description|  
|------------|-----------------|  
|[IDebugSourceServerModule::GetSourceServerData](../vs140/IDebugSourceServerModule--GetSourceServerData.md)|Retrieves an array of source server information.|  
  
## Requirements  
 Header: Msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll