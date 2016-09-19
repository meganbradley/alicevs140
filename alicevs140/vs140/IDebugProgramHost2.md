---
title: "IDebugProgramHost2"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 2c37b3aa-97a9-4665-8709-edd917f18cb1
caps.latest.revision: 13
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugProgramHost2
This interface provides host (process) information about a program.  
  
## Syntax  
  
```  
IDebugProgramHost2 : IUnknown  
```  
  
## Notes for Implementers  
 The debug engine implements this interface on the same object as the [IDebugProgram2](../vs140/IDebugProgram2.md) interface to provide information about the hosting process. This is an optional interface.  
  
## Notes for Callers  
 Call [QueryInterface](../vs140/QueryInterface.md) on an `IDebugProgram2` interface to obtain this interface.  
  
## Methods in Vtable Order  
 The following table shows the methods of `IDebugProgramHost2`.  
  
|Method|Description|  
|------------|-----------------|  
|[GetHostName](../vs140/IDebugProgramHost2--GetHostName.md)|Gets the title, friendly name, or file name of the hosting process of this program.|  
|[GetHostId](../vs140/IDebugProgramHost2--GetHostId.md)|Gets the process identifier of the hosting process of this program.|  
|[GetHostMachineName](../vs140/IDebugProgramHost2--GetHostMachineName.md)|Gets the name of the machine the hosting process of this program is running on.|  
  
## Requirements  
 Header: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [Core Interfaces](../vs140/Core-Interfaces.md)   
 [IDebugProgram2](../vs140/IDebugProgram2.md)