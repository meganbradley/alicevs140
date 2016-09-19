---
title: "IEnumDebugProcesses2"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 06a1368f-10f0-44eb-af61-e388c2327111
caps.latest.revision: 15
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IEnumDebugProcesses2
This interface enumerates the processes running on a debug port.  
  
## Syntax  
  
```  
IEnumDebugProcesses : IUnknown  
```  
  
## Notes for Implementers  
 A custom port supplier implements this interface to provide a list of processes running on a port.  
  
## Notes for Callers  
 Visual Studio calls [IDebugPort2::EnumProcesses](../vs140/IDebugPort2--EnumProcesses.md) to obtain this interface.  
  
## Methods in Vtable Order  
 The following table shows the methods of `IEnumDebugProcesses2`.  
  
|Method|Description|  
|------------|-----------------|  
|[Next](../vs140/IEnumDebugProcesses2--Next.md)|Retrieves a specified number of processes in an enumeration sequence.|  
|[Skip](../vs140/IEnumDebugProcesses2--Skip.md)|Skips a specified number of processes in an enumeration sequence.|  
|[Reset](../vs140/IEnumDebugProcesses2--Reset.md)|Resets an enumeration sequence to the beginning.|  
|[Clone](../vs140/IEnumDebugProcesses2--Clone.md)|Creates an enumerator that contains the same enumeration state as the current enumerator.|  
|[GetCount](../vs140/IEnumDebugProcesses2--GetCount.md)|Gets the number of processes in an enumerator.|  
  
## Remarks  
 Visual Studio uses this interface to populate the **Processes** window.  
  
## Requirements  
 Header: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [Core Interfaces](../vs140/Core-Interfaces.md)   
 [EnumProcesses](../vs140/IDebugPort2--EnumProcesses.md)