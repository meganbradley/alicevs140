---
title: "IDebugProgramDestroyEventFlags2"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: d384ff71-dc71-40b9-a871-801f8b6a3418
caps.latest.revision: 9
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugProgramDestroyEventFlags2
Enables a debug engine to override the default behavior of the [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] UI when you end a debug session.  
  
## Syntax  
  
```  
IDebugProgramDestroyEventFlags2 : IUnknown  
```  
  
## Notes for Implementers  
 This interface is implemented by debug engines. It is useful for hosts that might create and destroy multiple programs over the lifetime of a process.  
  
## Methods  
 The following table shows the methods of `IDebugProgramDestroyEventFlags2`.  
  
|Method|Description|  
|------------|-----------------|  
|[IDebugProgramDestroyEventFlags2::GetFlags](../vs140/IDebugProgramDestroyEventFlags2--GetFlags.md)|Retrieves the program destroy flags.|  
  
## Remarks  
 The default behavior of the [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] UI is to go back to design mode after all programs have sent a program destroy event. This interface enables a debug engine to change that behavior.  
  
## Requirements  
 Header: Msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll