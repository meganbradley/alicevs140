---
title: "IEnumDebugPrograms2"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 7fbb8fb7-db64-4546-a364-dc668430c8af
caps.latest.revision: 13
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IEnumDebugPrograms2
This interface enumerates the programs running in the current debug session.  
  
## Syntax  
  
```  
IEnumDebugPrograms2 : IUnknown  
```  
  
## Notes for Implementers  
 The debug engine (DE) implements this interface to provide a list of programs being debugged by the DE.  
  
## Notes for Callers  
 Visual Studio calls [IDebugProcess2::EnumPrograms](../vs140/IDebugProcess2--EnumPrograms.md) to obtain this interface. [IDebugEngine2::EnumPrograms](../vs140/IDebugEngine2--EnumPrograms.md) is not used by Visual Studio.  
  
## Methods in Vtable Order  
 The following table shows the methods of `IEnumDebugPrograms2`.  
  
|Method|Description|  
|------------|-----------------|  
|[Next](../vs140/IEnumDebugPrograms2--Next.md)|Retrieves a specified number of programs in an enumeration sequence.|  
|[Skip](../vs140/IEnumDebugPrograms2--Skip.md)|Skips a specified number of programs in an enumeration sequence.|  
|[Reset](../vs140/IEnumDebugPrograms2--Reset.md)|Resets an enumeration sequence to the beginning.|  
|[Clone](../vs140/IEnumDebugPrograms2--Clone.md)|Creates an enumerator that contains the same enumeration state as the current enumerator.|  
|[GetCount](../vs140/IEnumDebugPrograms2--GetCount.md)|Gets the number of programs in an enumerator.|  
  
## Remarks  
 Visual Studio uses this interface to:  
  
-   Populate the **Modules** window (by calling [IDebugProcess2::EnumPrograms](../vs140/IDebugProcess2--EnumPrograms.md) and then calling [IDebugProgram2::EnumModules](../vs140/IDebugProgram2--EnumModules.md) on each program).  
  
-   Populate the **Attach to Process** list (by calling `IDebugProcess2::EnumPrograms` and then calling [QueryInterface](../vs140/QueryInterface.md) on each [IDebugProgram2](../vs140/IDebugProgram2.md) interface to obtain an [IDebugEngineProgram2](../vs140/IDebugEngineProgram2.md) interface).  
  
-   Generate a list of DEs that can debug each program in the process (using [IDebugProgram2::GetEngineInfo](../vs140/IDebugProgram2--GetEngineInfo.md)).  
  
-   Apply Edit and Continue (ENC) updates to each program (by calling IDebugProcess2::EnumPrograms and then calling [IDebugProgram2::GetENCUpdate](../vs140/IDebugProgram2--GetENCUpdate.md)).  
  
## Requirements  
 Header: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [Core Interfaces](../vs140/Core-Interfaces.md)   
 [EnumPrograms](../vs140/IDebugEngine2--EnumPrograms.md)   
 [EnumPrograms](../vs140/IDebugProcess2--EnumPrograms.md)